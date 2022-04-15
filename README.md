## Cryptocurrency Wallet

![An image shows a wallet with bitcoin.](Images/19-4-challenge-image.png)

### Background

You work at a startup that is building a new and disruptive platform called Fintech Finder. Fintech Finder is an application that its customers can use to find fintech professionals from among a list of candidates, hire them, and pay them. As Fintech Finder’s lead developer, you have been tasked with integrating the Ethereum blockchain network into the application in order to enable your customers to instantly pay the fintech professionals whom they hire with cryptocurrency.

In this Challenge, you will complete the code that enables your customers to send cryptocurrency payments to fintech professionals. To develop the code and test it out, you will assume the perspective of a Fintech Finder customer who is using the application to find a fintech professional and pay them for their work.

### What You're Creating
To complete this Challenge, you will use two Python files, both of which are contained in the starter folder.

The first file that you will use is called fintech_finder.py. It contains the code associated with the web interface of your application. The code included in this file is compatible with the Streamlit library. You will write all of your code for this Challenge in this file.

The second file that you will use is called crypto_wallet.py. This file contains the Ethereum transaction functions that you have created throughout this module’s lessons. By using import statements, you will integrate the crypto_wallet.py Python script into the Fintech Finder interface program that is found in the fintech_finder.py file.

Integrating these two files will allow you to automate the tasks associated with generating a digital wallet, accessing Ethereum account balances, and signing and sending transactions via a personal Ethereum blockchain called Ganache.

Specifically, you will assume the perspective of a Fintech Finder customer in order to do the following:

Generate a new Ethereum account instance by using the mnemonic seed phrase provided by Ganache.

Fetch and display the account balance associated with your Ethereum account address.

Calculate the total value of an Ethereum transaction, including the gas estimate, that pays a Fintech Finder candidate for their work.

Digitally sign a transaction that pays a Fintech Finder candidate, and send this transaction to the Ganache blockchain.

Review the transaction hash code associated with the validated blockchain transaction.

Once you receive the transaction’s hash code, you will navigate to the Transactions section of Ganache to review the blockchain transaction details. To confirm that you have successfully created the transaction, you will save screenshots to the README.md file of your GitHub repository for this Challenge assignment.


## Technologies

This project leverages **[python version 3.9.7](https://www.python.org/downloads/)** with the following packages and modules:

* [pandas](https://pandas.pydata.org/docs/) - *version 1.3.2* - This was used to be able to easily manipulate dataframes and create dataframes.

* [Streamlit](https://streamlit.io/) - *version 0.84.2* - To be able to view the application into a web browser and that users can interact with the ledger.

* [Data Classes](https://docs.python.org/3/library/dataclasses.html) -This module provides a decorator and functions for automatically adding generated special methods to classes, which managed us to use class blocks into our code structure.

* [datetime](https://docs.python.org/3/library/datetime.html) - While date and time arithmetic is supported, the focus of the implementation is on efficient attribute extraction for output formatting and manipulation. In our case, we used this to be able to determine the UTC timezoon to create a time stamp in our blockchain.

* [typing](https://docs.python.org/3/library/typing.html)- This allows us to use the most fundamental support consisting of the types Any, Union, Tuple, Callable, TypeVar, and Generic.

* [hashlib](https://docs.python.org/3/library/hashlib.html)- This module implements a common interface to many different secure hash and message digest algorithms. In our application, we use SHA256 to return a hexdigest.

* [web3.py](https://web3py.readthedocs.io/en/stable/overview.html) - This is a Python library for connecting to and performing operations on Ethereum-based blockchains.

* [eth-tester](https://pypi.org/project/eth-tester/) - This is a Python library that provides access to the tools we’ll use to test Ethereum-based applications.

* [mnemonic](https://pypi.org/project/mnemonic/) - This is a Python implementation for generating a 12- or 24-word mnemonic seed phrase based on the BIP-39 standard.

* [bip44](https://pypi.org/project/bip44/) - This is a Python implementation for deriving hierarchical deterministic wallets from a seed phrase based on the BIP-44 standard.

* [Infura API](https://infura.io/register) - An API that provides instant access to the Ethereum network over HTTPS (i.e., the web). You will need to create an account with Infura.

---

## Installation Guide

### 1. Install the application, Streamlit and Web3.py into your dev or base environment:

`pip install streamlit`

`pip install web3==5.17`

`pip install eth-tester==0.5.0b3` or  `pip install eth-tester`

`pip install mnemonic`

`pip install bip44`

### 2. Use VSCODE to view and edit the fintech_finder.py

---

### Steps Involved

The steps for this challenge are broken out into the following sections:

* Write the code and Launch the Fintech Finder Application on Streamlit
* Sign and Execute a Payment Transaction
* Inspect the Transaction on Ganache

#### Step 1: Write the code and Launch the Fintech Finder Application on Streamlit

In this section, you'll import several functions from the `crypto_wallet.py` script into the file `fintech_finder.py`, which contains code for Fintech Finder’s customer interface, in order to add wallet operations to the application. For this section, you will assume the perspective of a Fintech Finder customer (i.e., you’ll provide your Ethereum wallet and account information to the application).

Once the code is complete you run the 'fintech_finder.py' on streamlit

Below is the screen shot of the streamlit interface

![overview](Images/overview.png)

#### Step 2: Sign and Execute a Payment Transaction

Fintech Finder customers will select a fintech professional from the application interface’s drop-down menu, and then input the amount of time for which they’ll hire the worker. Once you click on 'Send Transaction' you will see the `transaction_hash`  displayed on the application’s web interface.

Below is the screen shot of a signed transaction where we have selected Ash for 40 Hours, which turns out to a total of 13.20 Ether

![selection](Images/selection.png)


#### Step 3: Inspect the Transaction on Ganache

Verify whether the transaction is recorded on Ganache

a) Screenshot of the client's address balance and history on Ganache. 

![client](Images/client.png)

b) Screenshot of the transaction details on Ganache. 

![transaction](Images/transaction.png)

c) Screenshot of the recipient’s address balance and history from your Ganache application. 

![fintech](Images/fintech.png)

---

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Copyright © 2022 #Blockchain-Wallets

## Contributors

Contributed by: Gregg R. Saldutti

Email: greggnyc1@gmail.com
