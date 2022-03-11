# ND1309 C2 Ethereum Smart Contracts, Tokens and Dapps - Project Starter 
**PROJECT: Decentralized Star Notary Service Project** - For this project, you will create a DApp by adding functionality with your smart contract and deploy it on the public testnet.

### ToDo
This Starter Code has already implemented the functionalities you implemented in the StarNotary (Version 2) exercise, and have comments in all the files you need to implement your tasks.



### Dependencies
For this project, you will need to have:
1. **Node and NPM** installed - NPM is distributed with [Node.js](https://www.npmjs.com/get-npm)
```bash
# Check Node version
node -v
# Check NPM version
npm -v
```


2. **Truffle v5.X.X** - A development framework for Ethereum. 
```bash
# Unsinstall any previous version
npm uninstall -g truffle
# Install
npm install -g truffle
# Specify a particular version
npm install -g truffle@5.0.2
# Verify the version
truffle version
```


2. **Metamask: 5.3.1** - If you need to update Metamask just delete your Metamask extension and install it again.


3. [Ganache](https://www.trufflesuite.com/ganache) - Make sure that your Ganache and Truffle configuration file have the same port.


4. **Other mandatory packages**:
```bash
cd app
# install packages
npm install --save  openzeppelin-solidity@2.3
npm install --save  truffle-hdwallet-provider@1.0.17
npm install webpack-dev-server -g
npm install web3
```


### Run the application
1. Clean the frontend 
```bash
cd app
# Remove the node_modules  
# remove packages
rm -rf node_modules
# clean cache
npm cache clean
rm package-lock.json
# initialize npm (you can accept defaults)
npm init
# install all modules listed as dependencies in package.json
npm install
```


2. Start Truffle by running
```bash
# For starting the development console
truffle develop
# truffle console

# For compiling the contract, inside the development console, run:
compile

# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset

# For running unit tests the contract, inside the development console, run:
test
```

3. Frontend - Once you are ready to start your frontend, run the following from the app folder:
```bash
cd app
npm run dev
```

---

### Important
When you will add a new Rinkeyby Test Network in your Metamask client, you will have to provide:

| Network Name | New RPC URL | Chain ID |
|---|---|---|
|Private Network 1|`http://127.0.0.1:9545/`|1337 |

The chain ID above can be fetched by:
```bash
cd app
node index.js
```

## Troubleshoot
#### Error 1 
```
'webpack-dev-server' is not recognized as an internal or external command
```
**Solution:**
- Delete the node_modules folder, the one within the /app folder
- Execute `npm install` command from the /app folder

After a long install, everything will work just fine!


#### Error 2
```
ParserError: Source file requires different compiler version. 
Error: Truffle is currently using solc 0.5.16, but one or more of your contracts specify "pragma solidity >=0.X.X <0.X.X".
```
**Solution:** In such a case, ensure the following in `truffle-config.js`:
```js
// Configure your compilers  
compilers: {    
  solc: {      
    version: "0.5.16", // <- Use this        
    // docker: true,
    // ...
```

## Raise a PR or report an Issue
1. Feel free to raise a [Pull Request](https://github.com/udacity/nd1309-p2-Decentralized-Star-Notary-Service-Starter-Code/pulls) if you find a bug/scope of improvement in the current repository. 

2. If you have suggestions or facing issues, you can log in issue. 

---

Do not use the [Old depreacted zipped starter code](https://s3.amazonaws.com/video.udacity-data.com/topher/2019/January/5c51c4c0_project-5-starter-code/project-5-starter-code.zip)



###########

truffle migrate --reset --network rinkeby

Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



Migrations dry-run (simulation)
===============================
> Network name:    'rinkeby-fork'
> Network id:      4
> Block gas limit: 0x1c9c347


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > block number:        10312060
   > block timestamp:     1647034456
   > account:             0x4c277daEef7e3063f483B3FD424dD09DEFDfD5F0
   > balance:             0.49352989
   > gas used:            210237
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00420474 ETH

   -------------------------------------
   > Total cost:          0.00420474 ETH


2_deploy_contracts.js
=====================

   Deploying 'StarNotary'
   ----------------------
   > block number:        10312062
   > block timestamp:     1647034469
   > account:             0x4c277daEef7e3063f483B3FD424dD09DEFDfD5F0
   > balance:             0.44600099
   > gas used:            2349082
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.04698164 ETH

   -------------------------------------
   > Total cost:          0.04698164 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.05118638 ETH





Starting migrations...
======================
> Network name:    'rinkeby'
> Network id:      4
> Block gas limit: 0x1c9c380


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0x16ef78308ade1f9eacbec84f05e688b8c487bf6a9ef98188d5f3038509f41d01
   > Blocks: 1            Seconds: 8
   > contract address:    0x79484683db291890c50c5A370289D1673BeB3Cac
   > block number:        10312061
   > block timestamp:     1647034486
   > account:             0x4c277daEef7e3063f483B3FD424dD09DEFDfD5F0
   > balance:             0.49320389
   > gas used:            226537
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00453074 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00453074 ETH


2_deploy_contracts.js
=====================

   Deploying 'StarNotary'
   ----------------------
   > transaction hash:    0x4297c357c1cdd281d2e2a6305994cf33e83dc8943964bcd6d7f2e9747ddd5071
   > Blocks: 0            Seconds: 4
   > contract address:    0x00a5838491b881E229EEDaB817Dc6316d50FCFFc
   > block number:        10312063
   > block timestamp:     1647034516
   > account:             0x4c277daEef7e3063f483B3FD424dD09DEFDfD5F0
   > balance:             0.44400299
   > gas used:            2414282
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.04828564 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.04828564 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.05281638 ETH

