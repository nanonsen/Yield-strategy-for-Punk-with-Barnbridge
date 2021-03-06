# Yield-strategy-for-Punk-with-Barnbridge

Concept
=> Using Barnbridge's USDC Junior bond(variable APY) smart-yield product

**SMART Yield intro**
SMART Yield allows users to mitigate the variable yield volatility of other projects, such as Aave, Compound, or Yearn Finance, by introducing senior and junior tranche derivatives. Users are able to mint junior or senior tokens which represent accordingly-tranched deposits into the underlying protocol. Junior token holders provide the liquidity necessary for senior bond investors to be able to receive fixed yield. The risk present is that, should the underlying variable rate annuities fall below the level necessary to meet senior debt obligations, junior yields and potentially even principals would be algorithmically reallocated to cover. At the same time, juniors will benefit from the extra yield generated by senior deposits in cases where the variable rate of the underlying debt pool (including any associated token subsidy rewards) are higher than the weighted average guaranteed yields of current seniors. It is expected that the junior positions will have more capital in a given pool than the senior ones.
![image](https://user-images.githubusercontent.com/86796424/124805703-d4033300-df96-11eb-9183-1b0c798bfcd1.png)


# Strategy name
Punk annuity with Barn bridge's Junior bon product

# mechanism
1. Users deposit USDC into Punk protocol.
2. Use Punk's forge to deposit USDC (Junior bond) from Barnbridge's Smart-yield products.
3. BOND tokens are given and the final APY can be obtained.
4. An entity shall periodically invest in compound interest and pay a high return to Punktoken.
5. This can provide very high APY reliably.

------------------------------------------

## Barnbridge Installing

### Install NodeJS dependencies which include HardHat
    npm install
### Compile the contracts
    npm run compile
    
## Running Tests

    npm run test

## Running Code Coverage Tests

    npm run coverage

## MainNet Forking


    npm run test-mainnet    
    
## Deploying to Kovan testnet

### Use the code in the scripts folder to deploy the contracts on Kovan

    npx hardhat run --network kovan scripts/deploy-kovan-aave-dai.ts
    npx hardhat run --network kovan scripts/deploy-kovan-aave-usdc.ts
    npx hardhat run --network kovan scripts/deploy-kovan-aave-usdt.ts
    npx hardhat run --network kovan scripts/deploy-kovan-compound-dai.ts
    npx hardhat run --network kovan scripts/deploy-kovan-compound-usdc.ts
    npx hardhat run --network kovan scripts/deploy-kovan-cream-usdc.ts
    npx hardhat run --network kovan scripts/deploy-kovan-bondmodel-v2-compounded.ts

### Deploy the Bot to further test the live contracts!

    npx hardhat run --network kovan scripts/bot-kovan-oracle-update.ts 

    # Press ctl+c to stop
    
Source : https://github.com/nanonsen/BarnBridge-SmartYieldBonds
