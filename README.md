# Mystery Game
This is a small game programmed with a ETH smart contract, where you can either create and solve mysterys. 
* Note: Ropsten test net is now down. You need to find an alternative

Play the Game:  
- Set up new game
- give your answer under write, and getQuest. To get the first Quest enter: "0" or empty field
- find the quest and read and press mystery with your ETH address


# Set Up New game
To set up your own game you can deploy "setUpMystery" and add new Quest with "newQuest"

# Play the game
To play a newly setup game, you need to deploy "Mystery" with the previously created smart contract address. 

# Interact with Web3
To interact with the smart contract on https://ropsten.etherscan.io/, you need to verify your contract here: https://ropsten.etherscan.io/verifyContract


### To Do: 
To improve the security of the game the answer should be hidden.
This can be achieved when we add the hash of the results directly instead of the results and hash it on the chain.
E.g. This could be added in the following way:

function generateSealedAnswer(string answer) public pure returns(bytes32 sealedBid){sealedBid=keccak256(abi.encodePacked(answer));}
    
and remove function createHashFromAnswer(...){...}  accordingly
