## Deploying

Uses [Hardhat](https://hardhat.org/), as recommended in OpenZeppelin's [Deploying and interacting](https://docs.openzeppelin.com/learn/deploying-and-interacting) guide.

1. `cp .env.example .env` and adapt
2. `npx hardhat run scripts/deploy.js --network <rinkeby|mainnet>`

```javascript
[signer] = await ethers.getSigners()
contract = new ethers.Contract(address, abi, signer)
contract.pause()
contact.unpause()
```

## Verifying in Etherscan

1. Set `ETHERSCAN_API_KEY` in your `.env` file
2. Run ```npx hardhat verify --network <rinkeby|mainnet> <contract address> "<TOKEN_NAME>" "<TOKEN_SYMBOL>" "<TOKEN_INITIAL_SUPPLY>" "<TARGET_OWNER>"```
