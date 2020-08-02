//初始化创世区块
geth  --datadir data0 init genesis.json

//启动
geth --datadir data0 --rpc --rpcaddr=0.0.0.0 --rpcport 8545 --rpccorsdomain "*" --rpcapi "eth,net,web3,personl,admin,shh,txpool,debug,miner" --nodiscover --maxpeers 30 --networkid 101 --port 30303 --mine --miner.threads 1  --allow-insecure-unlock  console
//查看账号列表
eth.accounts

//创建账号
personal.newAccount()
//查看账号余额
eth.getBalance(eth.accounts[0])

//查看区块
eth.getBlock(0)

//查看矿工地址
eth.coinbase

//查看矿池
txpool.content
//查看块高
eth.blockNumber
