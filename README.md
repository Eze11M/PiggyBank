# PiggyBank sample solidity contract.

This repo contains a sample piggybank contract that selfdestructs when its balance is withdrawed.

## The contract features:

   1. A public address "owner" state variable that its initialized to the contract deployer address.
   2. An external payable "receive()" function that receives ETH from other wallets or contracts that call it.
   3. An external "withdraw()" function that selfdestructs the contract sending its balance to the owner which is the only who can call it.
   4. A customized event handling for both "receive()" and "withdraw()" functions.

## Advise:

Compiling this contract will raise a deprecation warning over "selfdestruct()" keyword functionality. As this projects code only purpouse is to practice, is strongly recommended not to copy and paste or use this keyword functionality as a reference for newer contracts. Its recommended, however, to implement different patterns such as pausable functions or update proxys depending the contract purpouse and needs.