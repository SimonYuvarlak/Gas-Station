# Account Types in Circle, SCA and EOA 

In this lesson, you will learn about the different types of accounts in Circle, a blockchain platform that supports smart contract execution and account abstraction. You will also learn how account abstraction works and how it enables users to pay gas fees with any token. Finally, you will learn about the role of gas stations, which are entities that facilitate gas payments for users. 

## Account Types in Circle 

You will learn about two types of accounts: `SCA` and `EOA` accounts. Each account type has different features and capabilities. 

SCA stands for Smart Contract Account. It is an account that is controlled by a smart contract code. It can send and receive transactions, store data, and execute logic. An SCA can also create other SCAs or EOAs. 

EOA stands for Externally Owned Account. It is an account that is controlled by a private key. It can send and receive transactions, but it cannot store data or execute logic. An EOA can only interact with SCAs by sending transactions to them. 


## Account Abstraction 

`Account abstraction (ERC-4337)` is a feature that allows users to pay gas fees with any token, instead of using the native token of the platform. This feature enables users to access a wider range of applications and services on the platform, without having to worry about the availability and volatility of the native token. 

Account abstraction works by allowing users to specify the token and the amount they want to use for gas fees in their transactions. The platform then verifies if the user has enough balance of that token in their account, and deducts the gas fees from their account accordingly. The platform also converts the gas fees from the token to the native token, and pays the validators who process the transactions. 

## Gas Station 

- A gas station is an entity that facilitates gas payments for users who want to use account abstraction. 
- A gas station acts as an intermediary between the user and the platform, by providing the user with a signed transaction that includes the gas fees in the native token. - The user then sends the signed transaction to the platform, and the platform executes it as if it was sent by the gas station. 

In this section, you will use gas station, so that you can transfer tokens without needing to have native tokens. 

To use gas station the account type must be SCA. 

In the testnet, gas station process is automatically handled meaning that you do not need the configuration but in the mainnet, you will need to set this up and also providing your credit card as the payment method. 

## Summary 

- There are two different account types: SCA and EOA 

- You can use gas station to sponsor gas fee of your users 

- To use gas station, the account type must be SCA 

 

 
