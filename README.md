# Blockchainpaymethod
Implementing payment methods with crypto currency

git pull --all
git branch

> c1_genesis_json
> c2_db_changes_txt
> c3_state_blockchain_component
> c4_caesar_transfer
> c5_broken_trust
> c6_immutable_hash
> c7_blockchain_programming_model
> c8_transparent_db
> c9_tango
> c10_peer_sync
> c11_consensus
> c12_crypto
> c13_training_network
> c14_why_transaction_costs_gas
> c15_blockchain_forks_what_why_how
> c16_blockchain_explorer

mkdir -p $GOPATH/src/github.com/web3coach
cd $GOPATH/src/github.com/web3coach

git clone https://github.com/web3coach/the-blockchain-bar.git

git pull --all

git checkout c1_genesis_json

go install ./cmd/...

tbb help

tbb run --help

Launches the TBB node and its HTTP API.

Usage:
  tbb run [flags]

Flags:
      --bootstrap-account string   default bootstrap Web3Coach's Genesis account with 1M TBB tokens (default "0x09ee50f2f37fcba1845de6fe5c762e83e65e755c")
      --bootstrap-ip string        default bootstrap Web3Coach's server to interconnect peers (default "node.tbb.web3.coach")
      --bootstrap-port uint        default bootstrap Web3Coach's server port to interconnect peers (default 443)
      --datadir string             Absolute path to your node's data dir where the DB will be/is stored
      --disable-ssl                should the HTTP API SSL certificate be disabled? (default false)
  -h, --help                       help for run
      --ip string                  your node's public IP to communication with other peers (default "127.0.0.1")
      --miner string               your node's miner account to receive the block rewards (default "0x0000000000000000000000000000000000000000")
      --port uint                  your node's public HTTP port for communication with other peers (configurable if SSL is disabled) (default 443)
      
      tbb wallet new-account --datadir=$HOME/.tbb

> Please enter a password to encrypt the new wallet:
> Password:

tbb version
> Version: 1.9.2-alpha  TX Gas

tbb run --datadir=$HOME/.tbb --ip=127.0.0.1 --port=8081 --miner=0x_YOUR_WALLET_ACCOUNT --disable-ssl

Launching TBB node and its HTTP API...
Listening on: 127.0.0.1:8081
Blockchain state:
- height: 0
- hash: 0000000000000000000000000000000000000000000000000000000000000000
Searching for new Peers and their Blocks and Peers: 'node.tbb.web3.coach:443'
Found 37 new blocks from Peer node.tbb.web3.coach:443
Importing blocks from Peer node.tbb.web3.coach:443...

Persisting new Block to disk:
{"hash":"000000a9d18730c133869d175a886d576df5675e0e73900bf072c59047b9d734","block":{"header":{"parent":"0000000000000000000000000000000000000000000000000000000000000000","number":0,"nonce":1925346453,"time":1590684713,"miner":"0x09ee50f2f37fcba1845de6fe5c762e83e65e755c"},"payload":[{"from":"0x09ee50f2f37fcba1845de6fe5c762e83e65e755c","to":"0x22ba1f80452e6220c7cc6ea2d1e3eeddac5f694a","value":5,"nonce":1,"data":"","time":1590684702,"signature":"0JE1yEoA3gwIiTj5ayanUZfo5ZnN7kHIRQPOw8/OZIRYWjbvbMA7vWdPgoqxnhFGiTH7FIbjCQJ25fQlvMvmPwA="}]}}

Persisting new Block to disk:
{"hash":"0000004d3faa1f7b8802aa809c8b77253859846602de3402a1bc67a0026cd94d","block":{"header":{"parent":"000000a9d18730c133869d175a886d576df5675e0e73900bf072c59047b9d734","number":1,"nonce":1331825342,"time":1592320406,"miner":"0x09ee50f2f37fcba1845de6fe5c762e83e65e755c"},"payload":[{"from":"0x09ee50f2f37fcba1845de6fe5c762e83e65e755c","to":"0x596b0709ed646e3e76b6c1fd58297b145b68387c","value":1000,"nonce":2,"data":"","time":1592320398,"signature":"1JIi9sYEZ+9RBG7IwACmm9vC4D7QVXqvBH1Es7cmeCJljTknVM80AzrhoLAW9RwCguunRO0qpN4JJ287VLFNfAE="}]}}
...
