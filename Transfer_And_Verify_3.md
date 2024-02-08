# Transfer and Verify

For this lesson, you will be using `Working-With-User-Controlled-Wallets` project.

Go ahead and open up the project.

## .env File

You will need to modify the .env file.

### Stays Same

Following fileds will remain the same.

- `API_KEY`
- `APP_ID`
- `USDC_TOKEN_ID`

### Modity

You will modify the following fields

- `USER_ID`: You should enter the new user id.
- `WALLET_ID`: This will be replaced with the new wallet's id.
- `ADDRESS`: This will be replaced with the new wallets's address.

## Check Wallet Status

As you did in the last section of this course, you are going to get the challenge id. The user will verify the challenge by entering his/her pin.

- Now, to get the wallet id, run the command `npm run check_wallet_status`. This command will return a response to the console.

The response will be something like:

```javascript
  "data": {
    "wallets": [
      {
        "id": "13cda487-0c8b-5812-8b95-59042d......",
        "state": "LIVE",
        "walletSetId": "018d846e-216e-794f-923e-f08c92ab80b5",
        "custodyType": "ENDUSER",
        "userId": "ae097766-5770-4407-805a-7879036c6818",
        "address": "0x3328477a6892e3bcf11d6de95370cc8ed03c11e8",
        "blockchain": "MATIC-MUMBAI",
        "accountType": "SCA",
        "updateDate": "2024-02-07T16:37:06Z",
        "createDate": "2024-02-07T16:37:06Z"
      }
    ]
  }
```

- Here, you will save `address` and `id` as `ADDRESS` and `WALLET_ID` to the .env file.
- As you can see, there is a filed called `accountType` with the value: `SCA`. This indicates that this account is type of `SCA`. That is what we were aiming for.

## Get Test USDC

- Go to the [faucet website](https://faucet.circle.com/?_gl=1*1h4wzev*_ga_GJDVPCQNRV*MTcwNzMyMDU3Ny40LjEuMTcwNzMyNDMwOS42MC4wLjA) and get test tokens like you did in the last section.
- Once the operation is successful, run the command `npm run check_balance`. You should see a similar response on the console, where the second token's (USDC) amount is 10.

## Initiate Transaction

Last time, you also had to get native token Matic for the gas fee. This time since you are using gas fee, the gas is sponsored and you can directly make the transfer. For that run the command `npm run initiate_transaction` which should return `user token`. `encryption key` and `challenge id`. Note this values.

## Complete the Challenge

- Since this is exactly the same process as before, this part also will be the same.
- In the `User-Contorolled-Wallet` project, click the wallet icon, where you call websdk.
- Below, you will enter the variables to complete the challange: `APP ID`, `User Token`, `Encryption Key` and `Challenge ID`.
- You will use the last three from thre result of initiate transaction response.

## Verify Transaction

This is also as same as before.

- Go to the Circle Website
- Open Transactions under User Controlled
- There, you should be able to find your transaction.
