# coin-flip-randomization-ctf
My solution for bypassing "random numbers" in solidity 

The aim is to guess the number 10 times. To actually do this we will need to create another contract using the instance address with a function that lets us flip the coin and mark it as correct. 

Firstly mimic the same logic and create of the instance. Make sure to deploy your fake contract to the originals instance address on rinkeby.
then create a function to flip the coin and always return it as the correct guess regardless if you guess correctly or not like so:

  uint256 coinFlip = uint256(blockValue/ FACTOR);   
        bool side = coinFlip == 1 ? true : false;         
        victimContract.flip(side);    

You can check your consecutive wins through the main contract and once you hit 10 thene just submit your answer
<img width="1536" alt="coinflip" src="https://user-images.githubusercontent.com/63403890/185659024-28e20c7d-3913-4612-8e84-e2bfe6b87aca.png">
