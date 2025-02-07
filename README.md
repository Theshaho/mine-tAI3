# mine-tAI3
mine tAI3 tokens using Taurus

in this guide we will mine tAI3 tokens using Taurus.

you need a subwallet substrate address.

```bash
mkdir taurus
```

```bash
cd taurus
```

Download Taurus node and farmer 
```bash
wget -L https://github.com/autonomys/subspace/releases/download/taurus-2024-nov-05/subspace-node-ubuntu-x86_64-v2-taurus-2024-nov-05
```

```bash
wgte -L https://github.com/autonomys/subspace/releases/download/taurus-2024-nov-05/subspace-farmer-ubuntu-x86_64-v2-taurus-2024-nov-05
```

make these files executable
```bash
chmod +x subspace-farmer-ubuntu-x86_64-v2-taurus-2024-nov-05
chmod +x subspace-node-ubuntu-x86_64-v2-taurus-2024-nov-05
```

replace <YOUR_NODE_NAME> with yours

```bash
./subspace-node-ubuntu-x86_64-v2-taurus-2024-nov-05 \
  run \
  --chain taurus \
  --base-path "/root/taurus" \
  --name "<YOUR_NODE_NAME>" \
  --farmer
```

start Taurus farmer 

Replace <WALLET_ADDRESS> with your wallet address starts with suc..., use [ss58.org](https://ss58.org/) copy your Dot address and then use custom prefix with `6094` 

Replace <PATH_TO_FARM> with the directory where you want to store the plot

Replace <PLOT_SIZE> with the size of the plot (e.g. 10GB, 2TiB)

```bash
./subspace-farmer-ubuntu-x86_64-skylake-taurus-2024-nov-05 farm \
  --reward-address <WALLET_ADDRESS> \
  path=/root/taurus,size=<PLOT_SIZE>
```

once the farmer is started you can monitor your wallet address [here](https://astral.autonomys.xyz/taurus/consensus/accounts/)

## Join our Telegram Channel

For more bots and tutorials you can join our Telegram channel

[**UbuntuForNodes**](https://t.me/ubuntufornodes)

also you can follow me on [X(iamshaho)](https://x.com/iamshaho)

[source](https://docs.autonomys.xyz/farming/cli/taurus/)
