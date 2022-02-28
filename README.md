1. Users can enter lottery with ETH based on a USD fee
2. An admin will choose when the lottery is over
3. The lottery will select a random winner 

How do we want to test this?

    1. `mainnet-fork`
    2. `development` with mocks 
    3. `testnet`
# Setup
    First step setting up your project: 
    1. `brownie init`
           
        or use[chainlink-mix](https://github.com/smartcontractkit/chainlink-mix)
       
    2. `brownie bake chainlink-mix & mv chainlink (project_name)`

# Other Files
    Create `dot.env` file inside your project's directory and include the following:
        `export PRIVATE_KEY_1 = PRIVATE_KEY_1`
        `export WEB3_INFURA_PROJECT_ID = PROJECT_ID`
        `export ETHERSCAN_TOKEN = API_TOKEN`
    
    In order to encrypt your private key, add it to Brownie:
        `brownie accounts new <account_id>`

# Usage

   ## Compile
      `brownie compile`
    
   ## Test
      `brownie test --network <choose_network> -s`
    
   ## Deploy
      `brownie run scripts/deploy_lottery.py --network <choose_network>`
