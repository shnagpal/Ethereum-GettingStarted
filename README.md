# Ethereum-GettingStarted

# Installations
~~~~~
sudo apt-get install software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install ethereum
sudo apt-get install solc
~~~~~

# Create genesis file
Write genesis.json:
~~~~~
{
  "nonce": "0x0000000000000123",
  "timestamp": "0x0",
  "parentHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "extraData": "0x0",
  "gasLimit": "0x8000000",
  "difficulty": "0x400",
  "mixhash": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "coinbase": "0x3333333333333333333333333333333333333333",
  "alloc": {}
}
~~~~~

Initialize the first block:
~~~~~
geth init genesis.json
~~~~~

# Create geth account
To create a new account:
~~~~~
geth account new
~~~~~
Enter password for your account

# Run geth node
~~~~~
geth --datadir ~/.ethereum  --mine --minerthreads=2 --networkid 54321 --rpc --rpcport "8545" --rpccorsdomain "*" --port "30303" --nodiscover --rpcapi eth,net,web3 --autodag  --nat "any" --unlock 0
~~~~~

# Connect to geth node
~~~~~
geth attach
~~~~~
You will enter geth console where you can invoke web3 calls
