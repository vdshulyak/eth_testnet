ETH_Testnet has been setup for ETH currency
Network can be started with following commands : 

1. "C:/Program Files/Geth/geth.exe" --datadir node1 --unlock "0x1cDBe2Ba2F320fdeD74A1c89cDDE2457fb44c49a" --port 30304 --mine --miner.threads=1  
2. "C:/Program Files/Geth/geth.exe"  --datadir node2 --unlock "0xdb4D540Cb3FC5255145D9Ad2506Ba66B1b4a8FC9" --port 30305 --rpc --bootnodes "enode://8e5c5ed2b9b54b4284342cefeebdb46ca1d268f4ce9deee480904524b644fae2c0d44ddaa148f2884861b0a8a3ad83461f420a81083d033d164293affa9b21c0@127.0.0.1:30304" --ipcdisable --allow-insecure-unlock --mine --miner.threads=1

Command 1 starts first node. Since the node has been initialized already, --unlock flag hjust unlocks it. --mine and dependend on it --miner.threads parameter makes nod do mining work
Command 2 is initialized using same command. enode flag taken from first command is specified in initialization so nodes can talk to each other.