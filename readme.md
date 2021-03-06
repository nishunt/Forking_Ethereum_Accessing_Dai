# Frok Ethereum Network with Ganache

## Overview

In this project, I fork the ethereum mainnet in real time using ganache and access the Dai contract.
Then, access the account on mainnet having the most no. of dai, and transfer all the Dai from his account to a dummy account.
All this happens on a local mirror of the mainnet, that we have created using ganache.

## Process Flow:
0. Find the account holding most DAIs on mainnet using Ethplorer.io, lets call it daiHolder.
1. Clone Ethereum Mainnet Using Ganache CLI and Infura, Unlock daiHolder's account with Ganache, using below code:

        npm install -g ganache
        ganache --fork -u "0xd9e..."

2. Access the DAI smart contract using its Address and ABI.
3. Send the total balance of daiHolder to our account using Transfer function from ERC20.

The code for step 2 and 3 is written in script.js file, to run it, after following step 1,
type the below code in the terminal being in the folder where you have cloned this project:

    node script.js

