
# Starknet Counter

This is an onboarding project with Cairo Language to deploy a smart contract in starknet-devnet.

## Environment

- nodejs: v22.7.0
- scarb 2.6.5 (d49f54394 2024-06-11)
- cairo: 2.6.4 (https://crates.io/crates/cairo-lang-compiler/2.6.4)
- sierra: 1.5.0
- starkli 0.3.4

## Environment Variables

To run this project, declare the following environment variables:

```
export STARKNET_ACCOUNT=".c-wallets/account0_account.json"
export STARKNET_KEYSTORE=".c-wallets/account0_keystore.json"
export STARKNET_RPC="http://127.0.0.1:5050"
```

## Deployment

To deploy this project, first run the starknet-devnet:

\> `starknet-devnet --seed 2525635640`

Declare the contract on the starknet-devnet to create a class in the net:

\>`starkli declare target/dev/counter_CounterContract.contract_class.json`

To finish, you can create an instance of the class declared using the class' hash:

\>`starkli deploy [class hash] [constructor arguments]`

\>`starkli deploy 0x01366464e49982b8fdb63f164a75690446930d7566b84baef05733029f7d0657 0x12`


## Running Tests

Reading a smart contract:
\>`starkli call 0x04247fba5a771ce41877feac3fa1e23e0b49511790a3b473a57a3e53207d0d1a get_contador`

Writing in a smart contract:
\>`starkli invoke 0x04247fba5a771ce41877feac3fa1e23e0b49511790a3b473a57a3e53207d0d1a increase_contador`

For this project, you can use any password you want (such as 123456) to invoke the functions.

## Screenshots

![image](https://github.com/user-attachments/assets/8d95ce54-a6b5-42ed-9a61-41d614d221b9)


## Author

- [@Sergio Scripnic](https://www.github.com/SScripnic)
 

## Acknowledgements

 - [Preparando o Ambiente de Desenvolvimento Starknet](https://medium.com/starknet-in-brazil/preparando-ambiente-de-desenvolvimento-starknet-9e0663c1e0e5)

## 🛠 Skills
Cairo Language

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
