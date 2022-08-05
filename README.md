# Crypto Payment Application
This program is an application that users can run to find fintech professionals from among a list of candidates, hire them, and pay them. The program integrates the Ethereum blockchain network to enable users to pay the professionals whom they hire with cryptocurrency.

----

## Technologies
This application is written in the Python programming language. The code is edited in Visual Studio Code. The Python libraries, tools, and modules used in this application are: Streamlit, web3, bip44, dataclasses, typing, dotenv, os, & requests.

[Streamlit](https://docs.streamlit.io/), [web3](https://web3py.readthedocs.io/en/stable/), [bip44](https://pypi.org/project/bip44/), [dataclasses](https://docs.python.org/3/library/dataclasses.html), [typing](https://docs.python.org/3/library/typing.html), [dotenv](https://pypi.org/project/python-dotenv/), [os](https://python101.pythonlibrary.org/chapter16_os.html), [requests](https://requests.readthedocs.io/en/latest/)


----

## Installation Guide (NEEDS UPDATE)
For the user to run their own version of this program, they must generate their own key pair using a personal mnemonic seed phrase. This can be changed in the SAMPLE.env file. 

For the program to run correctly, the user must make sure that all libraries and modules are correctly imported in the beginning of the code. In the crypto_wallet.py file the imports should be:

    import os
    import requests
    from dotenv import load_dotenv
    load_dotenv()
    from bip44 import Wallet
    from web3 import Account
    from web3 import middleware
    from web3.gas_strategies.time_based import medium_gas_price_strategy

In the fintech_finder.py file the imports should be;

    import streamlit as st
    from dataclasses import dataclass
    from typing import Any, List
    from web3 import Web3
    w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545'))


----

## Usage

**The program is comprised of 3 main parts:**

1. Import Ethereum Transaction Functions into the Fintech Finder Application

Complete the following steps:
    1. Add the user's special mnemonic seed phrase to the SAMPLE.env file. When that is updated, rename the file .env
    2. Open the fintech_finder.py file and import the functions: `generate_account`, `get_balance`, & `send_transaction`
    3. Within the Streamlit sidebar section of code, create a variable named `account`. Set this variable equal to a call on the `generate_account` function
    4. Within the same section, define a new `st.sidebar.write` function that will display the balance of the customer’s account. Inside this function, call the `get_balance function` and pass it your Ethereum `account.address`

2. Sign and Execute a Payment Transaction

3. Inspect the Transaction

----

## Contributors

Arlie Jones

[E-mail](arliejones98@gmail.com)  |  [LinkedIn](https://www.linkedin.com/in/arlie-jones-020092159/)

----

## License

None