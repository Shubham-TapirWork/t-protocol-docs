# tech spec example 1


## Components

For proper working of this infrastructure we need following components:

### Smart Contracts

**Ethereum**

1. **Deposit Contract(_Ethereum_):** This contract is responsible for taking all the ETH and ETH derivative deposit from the users and storing the sharePrice. It passes the messages to Message Contract for passing of message. The deposit contract will look something like this:
    
    ```solidity
    contract Deposit{
    	uint256 public sharePrice;
    	function deposit(address _tokenAddress, address _receiver, uint256 _value, uint256 _destId) external payable;
    	function executeStrategies(address[] _strategyAddress,bytes[] memory _executionData,uint256[] _value) external;
    }
    ```
    
2. **Strategy Manager Contract:** This contract is responsible for managing all the staking/restaking/BnL etc. strategies. It further helps in execution of the strategies. It looks something like the following:
    
    ```solidity
    contract StrategyManager{
      struct StrategyStruct{
    	   uint256 ethDeposited;
         uint256 rewardsEarned;
         uint256 ethWithdrawn;
      }
      mapping(address=>address) public strategies;
      mapping(address=>StrategyStruct) public strategyDeposits;
    	function addStrategies(address _strategy) external;
    	function updateStratgy(address _strategy, StrategyStruct memory _changeBalane) external;
    }
    ```
    
3. **Strategy Contracts(_Ethereum_):** This contract is responsible for staking/restaking etc ETH on Ethereum on different protocols. Whenever a new protocol is whitelisted for staking, a new strategy contract is created and deposit contract delegates the calls to this contract whenever it has to interact with the protocol:
    
    ```solidity
    // This is a sample strategy actual strategies can look different
    abstract contract Strategy{
    	address public constant StakingAddress;
    	address public constant TOKEN_ADDRESS;
    	function tokenPrice() external view returns(uint256);
    	// apart from this all function depends on the strategy that needs to be executed
    }
    ```
    
4. **Messaging Contract:** This contract is responsible for sending message from L1 to L2. It uses LayerZero and other messaging protocol to do so. The Messaging Contract looks like this:
    
    ```solidity
    contract MessagingApp{
    	address public lzEndpoint;
    	address public Deposit;
    	function sendMessage(bytes memory _data, uint256 _destID) external onlyDeposit
    	function receiveMessage(bytes memory _data) external onlyDeposit
    }
    ```
    
    The messaging contract uses following typeIds to know what kind of transaction it is:
    
    ```solidity
        id=1 deposit
        id=2 rewards
        id=3 withdrawal
        id=4 L2 deposit received
    ```
    
5. **Withdrawal Contract:** This contract is responsible for creation of withdrawal queues and giving users their deposit back once the assets are withdrawn from strategies. It looks something like this:
    
    ```solidity
    contract Withdrawal{
    	address public MessagingApp;
    	Struct WithdrawalRequest{
    		uint256 timeCreated;
    		uint256 value;
    	}
    	mapping(address=>WithdrawalRequest) withdrawalQueue;
    	
    	function createWithdrawalRequest(address _receiver, uint256 _value) external onlyMessagingApp;
    	function claimWithdrawal(address _receiver, uint256 _value) exernal
    }
    ```
    

**Layer 2**

1. **Deposit Contract:** This contract is responsible for taking user deposits on Layer2 and minting the representative token. Depending on the asset deposited the shares are minted and the asset is deployed to respective strategy
    
    ```solidity
    contract DepositL2{
    	mapping(address=>cValue) whitelistedToken;
    	function deposit(address _tokenAddress, address _receiver, uint256 _value, uint256 _depositFee) external payable
    	function transferDepositL1(address _tokenAddress, uint256 _value) external;
    }
    ```
    
2. **nETH Contract:** This is the native ETH contract present on L2 that mints the native ETH token
    
    ```solidity
    contract nETH is ERC20{
    	function mintNETH(address _receiver, uint256 _value) external onlyAuthorised; 
    	function burnNETH(address _receiver, uint356 _value) external onlyAuthorised;
    }
    ```
    
3. **Messaging L2 Contract:** This contract is responsible for sending message from L2 to L1. It uses LayerZero and other messaging protocol to do so. The Messaging Contract looks like this:
    
    ```solidity
    contract MessagingApp{
    	address public lzEndpoint;
    	address public Deposit;
    	function sendMessage(bytes memory _data, uint256 _destID) external onlyDeposit
    	function receiveMessage(bytes memory _data) external onlyDeposit
    }
    ```
    

### Fee Module Nexus

The fee charged by Nexus consists of three parts:

1. **OnboardingFee:** This fee is charged from users whenever they deposit on nexus native yield contract. It’ll be a portion of funds deposited by the user.
2. **WithdrawalFee:** This fee is charged from users whenever they withdraw on nexus native yield contract. It’ll be a portion of funds withdrawn by the user.
3. **ManagementFee:** This fee is charged from the rewards earned as a management fee for executing strategies, sending rewards to the protocol and rebalancing the assets in the deposit contract.

This is implemented in Nexus Fee contract. It looks like:

```solidity
contract NexusFee{
    uint256 public onboardingFee=0;
    uint256 public withdrawalFee=0;
    uint256 public maintenanceFee=0;
    function changeFee(uint256 _onboardingFee,uint256 _withdrawalFee,uint256 _maintenanceFee) external;
    function collectFee(address _tokenAddress,uint256 _value) external payable;
}
```

> _Initially all the fees will be zero and overtime the Nexus DAO will define how the fees should be charged_

### Messaging between chains

For Nexus Network to enable cross chain native yields, it’ll need messaging protocol to send messages across various L2’s. There are two ways to do it:

1. **External messaging bridge(eg.LayerZero):** This way the Nexus can give yields and help user hold their native assets on any chain possible
2. **L2 Canonical Bridge:** This is more economical and secure way to send a message. But, this approach limits as to which chains Nexus Network can integrate with

While both the solutions are viable, the second one results in significant time delay from L2-L1 transfers. Thus, Nexus implements both for a better user experience.

### Offchain Oracle

offchain oracles are responsible for executing strategies, getting rewards and transferring L2 deposits to L1 deposit contract. So, in a nutshell it is very important component of the protocol. Let’s break down how it works in different contexts:

1. **Rewards**: After every few epoch as decided by the bot, the bot triggers reward calculation which means, the rewards that are earned by different strategies are transferred to Deposit Contract on L1. Then the sharePrice is calculated depending on the rewards earned and relayed on different Layer2 Deposit Contracts
2. **Transferring L2 deposits to L1:** Users are able to deposit ETH or derivative ETH that they have bridged previously to our contract. These deposits needs to be batched and transferred to L1 deposit contract as they earn yields on L1 itself through various strategies.
3. **Executing Strategies:** The bot is also responsible for executing strategies and sending respective tokens to the strategies. These strategies then earn rewards which are distributed back to the users.
