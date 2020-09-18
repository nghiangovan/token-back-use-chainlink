<h1 align="center">Welcome to CashBack 👋</h1>
<p align="center">
  <img src="https://img.shields.io/badge/version-1.0-blue.svg?cacheSeconds=2592000" />
</p>

![](/imageReadme/cover.png)

## Project setup (testnet)

#### Setup contract :

- Load dependencies:

```
cd contract
yarn install
```

- Copy .env file:

```
//LOCAL
//Local uses account one103q7qe5t2505lypvltkqtddaef5tzfxwsse4z7 on Shard 0
LOCAL_PRIVATE_KEY='45e497bd45a9049bcb649016594489ac67b9f052a6cdf5cb74ee2427a60bf25e'
LOCAL_MNEMONIC='urge clog right example dish drill card maximum mix bachelor section select'
LOCAL_0_URL='http://localhost:9500'

//TESTNET
//Account: one18t4yj4fuutj83uwqckkvxp9gfa0568uc48ggj7
TESTNET_PRIVATE_KEY='01F903CE0C960FF3A9E68E80FF5FFC344358D80CE1C221C3F9711AF07F83A3BD'
TESTNET_ADDRESS = 'one18t4yj4fuutj83uwqckkvxp9gfa0568uc48ggj7'
TESTNET_MNEMONIC='urge clog right example dish drill card maximum mix bachelor section select'

TESTNET_0_URL='https://api.s0.b.hmny.io'
TESTNET_1_URL='https://api.s1.b.hmny.io'

//MAINNET
//Please replace MAINNET_PRIVATE_KEY and MAINNET_MNEMONIC with your own!
//Account: one18t4yj4fuutj83uwqckkvxp9gfa0568uc48ggj7
MAINNET_PRIVATE_KEY='01F903CE0C960FF3A9E68E80FF5FFC344358D80CE1C221C3F9711AF07F83A3BD'
MAINNET_MNEMONIC='urge clog right example dish drill card maximum mix bachelor section select'
MAINNET_0_URL='https://api.s0.t.hmny.io'

GAS_LIMIT=3321900
GAS_PRICE=1000000000
```

- Deploy contract:

**Note:** Config in **contract/scripts/\*** to deploy in TESTNET

- You must change network **ChainID.HmyMainnet** -> **ChainID.HmyTestnet**
- MAINNET_PRIVATE_KEY -> TESTNET_PRIVATE_KEY
- MAINNET_0_URL -> TESTNET_0_URL

```
yarn all
```

#### Setup client:

- Load dependencies:

```
cd client
yarn install
```

- Run

```
yarn serve
```
