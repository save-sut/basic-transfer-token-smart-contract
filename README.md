[![https://github.com/save-sut/basic-transfer-token-smart-contract](https://res.cloudinary.com/tyroz/image/upload/v1640084190/Screen_Shot_2564-12-21_at_17.54.35_ufzrmi.png "https://github.com/save-sut/basic-transfer-token-smart-contract")](https://res.cloudinary.com/tyroz/image/upload/v1640084190/Screen_Shot_2564-12-21_at_17.54.35_ufzrmi.png)

# Prerequisites
1. [Git](https://nodejs.org/)
2. [Node.js](https://nodejs.org/)
3. [MetaMask](https://metamask.io/)

# How to run
1. Clone the repo
```sh
git clone https://github.com/save-sut/basic-transfer-token-smart-contract.git
```

2. Install the dependencies
```sh
npm install
```

3. You can get access to Ropsten by signing up with [Infura](https://infura.io/dashboard) and replace `Project ID` in `${INFURA_PROJECT_ID}` at `hardhat.config.js`

4. Get a test Ether: [Ropsten Ethereum Faucet](https://faucet.ropsten.be/)

5. Get the private key, You can export private key from MetaMask and replace in `${PRIVATE_KEY}` at `hardhat.config.js`

[![dev.to/dabit3](https://res.cloudinary.com/practicaldev/image/fetch/s--_g7R_Fdh--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/deod3d6qix8us12t17i4.jpg "dev.to/dabit3")](https://res.cloudinary.com/practicaldev/image/fetch/s--_g7R_Fdh--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/deod3d6qix8us12t17i4.jpg)

6. Compile and Deploy smart contract:
- Compile script:
```
npx hardhat compile
```
- Deploy to Ropsten Network or
```
npx hardhat run scripts/deploy.js --network ropsten
```
- Deploy to BSC Testnet
```
npx hardhat run scripts/deploy.js --network bscTestnet
```

7. Result in your Terminal:
```
Deploying contracts with the account: TOKEN_METAMASK_ADDRESS
Greeter deployed to: GREETER_ADDRESS
Token deployed to: TOKEN_ADDRESS
```

8. Copy `GREETER_ADDRESS` and `TOKEN_ADDRESS` from Terminal and replace at `src/App.js` on line 8-9

9. Open a new Terinal and Run script:
```
npm start
```

10. See the app in your browser
> Note[1/2]:
<b>Fetch Greeting:</b> Fetch the current greeting and log it out to the console.
<b>Set Greeting:</b> Update the greeting by signing the contract with your MetaMask wallet.
<b>Get Balance:</b> See your have 1,000,000 coins in our account logged out to the console.

You should also be able to view coin in MetaMask by clicking on Add Token:
[![dev.to/dabit3](https://res.cloudinary.com/practicaldev/image/fetch/s--bYhSNJ4P--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0t2ip26i5d2ltjc9j2a6.jpg "dev.to/dabit3")](https://res.cloudinary.com/practicaldev/image/fetch/s--bYhSNJ4P--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0t2ip26i5d2ltjc9j2a6.jpg)

Next click on Custom Token and enter the token contract address and then Add Token. (if asked for token decimals, choose 18) Now the tokens should be available in your wallet:
[![dev.to/dabit3](https://res.cloudinary.com/practicaldev/image/fetch/s--tLmPpIH8--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5op32iqbeszizri72qc0.jpg "dev.to/dabit3")](https://res.cloudinary.com/practicaldev/image/fetch/s--tLmPpIH8--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5op32iqbeszizri72qc0.jpg)

> Note[2/2]:
<b>Send Coins:</b> you can sending these tokens to other addresses.
You will need to Entering the Wallet Address in the Account ID field and the number of coins in Wei (amount * 10^18) in the Amount field.

# More detail and Referrence
[The Complete Guide to Full Stack Ethereum Development - Nader Dabit](https://dev.to/dabit3/the-complete-guide-to-full-stack-ethereum-development-3j13)
