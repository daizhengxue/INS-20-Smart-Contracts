## Project Introduction

This project modifies the mainnet contract based on INS20. We have removed the hard-coded parts to allow issuers more freedom in token issuance and asset deployment.

### How to Use

When deploying the contract, you need to input the following parameters:

- tick: The token symbol, for example, "INS".
- maxSupply: The maximum supply of the token, such as 21000000.
- mintLimit: The maximum amount for each minting, for example, 1000.
- proxy: The proxy address, which is an Ethereum address used to perform certain special contract operations.

### Example
Here is an example of deploying the contract:
```
const INS20 = artifacts.require("INS20");
module.exports = function(deployer) {
  deployer.deploy(INS20, "INS", 21000000, 1000, "0xYourProxyAddress");
};
```
In this example, we deploy a new INS20 contract with the token symbol "INS," a maximum supply of 21000000, a mint limit of 1000 per mint, and the proxy address as "0xYourProxyAddress."

Note that you should replace "0xYourProxyAddress" with your own proxy address.

### Conclusion

I hope this modified INS20 contract will help you better manage your project issuance and asset deployment. If you have any questions or suggestions, please feel free to provide feedback.
