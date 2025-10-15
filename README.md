## Base Greeter

Contract Deployed at URL: https://sepolia.basescan.org/address/0xfd8630194e4ca4a3bec21b7ed68828874e2c81b3

### Commands used

To compile

```
forge build
```

To deploy

```
forge create src/Greeting.sol:Greeter --rpc-url $BASE_SEPOLIA_RPC_URL --broadcast --private-key $PRIVATE_KEY --constructor-args "Hello I am a Base Builder"
```

To verify contract

```
forge verify-contract --chain base-sepolia $DEPLOYED_CONTRACT_ADDRESS src/Greeting.sol:Greeter --verifier etherscan --etherscan-api-key $_API_KEY --constructor-args $(cast abi-encode "constructor(string)" "Hello I am a Base Builder!")
```

Sourcing .env after saving it

```
source .env
```
