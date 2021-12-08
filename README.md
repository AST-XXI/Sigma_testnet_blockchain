# Sigma Testnet Blockchain

Sigma blockchain is a private testnet. This private network will help explore the potential for blockchain at ZBank.

Proof of Authority Development Chain: What is PoA?
The Proof of Authority (PoA) algorithm is a private blockchain networks. It requires pre-approval of, or voting in of, the address in order to send and receive transaction.
___

## Enviorment Setup

>## Step 1: is to set up our enviorment. For this we will need to download the Go Ethereum tool. [Click here: Geth](https://geth.ethereum.org/downloads/)
>
> Please be sure to choose your corresponding operating system.
![geth](Screenshots\geth.JPG)
>

___

>## Step 2: Download "Geth & Tools 1.9.7", be sure to select either 64 or 32 bit based on your computer
>
> ![geth](Screenshots\geth2.JPG)
>

___

>## Step 3: Extract the contents of the file onto a folder
>
> ![geth](Screenshots\geth3.JPG)
>

___

## Creating and initialize the node

> ## Step 4: Create new accounts for two nodes for the network
>
> These 2 new accounts will be used as pre-approved sealer addresses.
> Open Gitbash in Sigma_blockchain_testnet
> Be sure to write down the password that was input for the public key. this password will be used >to accesses funds on MyCrypto
> Use Command to create a new node:
>
>```bash
>./geth --datadir node1 account new
>./geth --datadir node2 account new
>```
>
>![geth](Screenshots\geth4.1.JPG)
>
>```bash
>./geth --datadir node2 account new
>```
>
>![geth](Screenshots\geth4.2.JPG)
____

>## Step 5: Generate gensis block
>
> Use Command to run code ./puppeth
>
>netowrk name: sigmablok
>
>```bash
>./puppeth
>```
>
>1. Type in 2 to configure new genesis.
>
>2. Create new genesis from scratch, Type 1
>3. Clique- proof-of-authority
>
>![geth](Screenshots\geth5.JPG)
>
>4. Insert accounts that are allowed to seal and which accounts that will be >prefunded.
>
>5. Specify chain/network ID
>
>6. Manage existing genesis and Export genesis configurations
>
>![geth](Screenshots\geth5.1.JPG)
>
> Use Command to initialize node2:
>
>```bash
>./geth init sigmabock.json --datadir node2
>```
>
___

>## Step 6: Initialize the nodes with the genesis json file
>
>Using geth, initialize each node with the new networkname.json
>
>```bash
>./geth --datadir node1 init sigmablok.json
>./geth --datadir node2 init sigmablok.jsons 
>```
>
>![geth](Screenshots\geth6.JPG)
>
___

> ## Step 7: Use Command to create local node
>
> We are required to use the first account in this code. The account address starts with 0x.
>
>```bash
>./geth --datadir node1 --unlock "0xe34Ee0dD61351005486901F5fA637351C9bcc198" --mine --rpc --allow-insecure-unlock
>```
>
>We will need to locate the Enode, which will be used as a pointer to the 2nd node.
>
>```bash
>for this example the endnode is: enode://515bb55f27f88ae3a9c0b319752a93f8d92f67ee39efd17c6eba7b561f17e84aaf34b5bba06cc3e61f933ec2d6e41e84335439e52dd0193b1ea20e90eaea806f@127.0.0.1:30303
>```
>
>![geth](Screenshots\geth7.1.JPG)
>
>## 2nd Node
>
> ## Step 7: we will need to start the new terminal in Blockchain-Tools (Sigma_blockchain_testnet)
>
>This step requires the endnode that was located in the previous step and the  the second account number. The account address starts with 0x.
>
>```bash
>./geth --datadir node2 --unlock "0x776A4247cA8F313cd84fE34ebaF538462dc8Edd6" --mine --port 30304 --bootnodes "enode://515bb55f27f88ae3a9c0b319752a93f8d92f67ee39efd17c6eba7b561f17e84aaf34b5bba06cc3e61f933ec2d6e41e84335439e52dd0193b1ea20e90eaea806f@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
>```
>
>![geth](Screenshots\geth7.2.jPG)
___

> ## Connecting SigmaBlok Network to MyCrypto
> To download MyCrypto app [CLICK HERE](https://download.mycrypto.com/) 
>
> Open MyCrypto app and connect to Sigma PoA
>
>![geth](Screenshots\geth8.jPG) ![geth](Screenshots\geth9.jPG)
>
>```bash
>Node Name: sigmablok
>Network Name: sigmablok
>Network: Custom
>Currency: ETH
>Chain ID: 1121 
>url: http://127.0.0.1:8545
>```
>
>![geth](Screenshots\geth10.jPG)
_______________

>## Connecting wallet and sending transaction: 
> To accesses wallet and funds you will need Keystore File that can be found in Node1, import key to MyCrypto.
>```bash
>Example: "UTC-- 2021-12- ...."
>```
>
>This step requires the password that was previously created for the wallet.
>
>![geth](Screenshots\geth11.1.jPG) ![geth](Screenshots\geth11.2.jPG)
>
_____
> ## Sending Transaction: 
>Step 1: Address of the recipient is needed.
>
>Step 2: input desired amount (ETH)
>
>Step 3: Transaction Fee can be adjusted (optional)
>
>Step 4: Be Sure to verify before sending transation.
>
>![geth](Screenshots\geth12.jPG)
>
>## Recent Transaction: 
> Click on tab "Recent Transaction" to check status of transaction.
>
>![geth](Screenshots\geth12.1.jPG)

## Congratulations! You Made Your Transaction on Sigma Blockchain. 
