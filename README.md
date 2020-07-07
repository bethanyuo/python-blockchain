# Python Blockchain

Learn how Blockchain networks work by building a simple one in Python. Blockchain is an immutable, sequential chain of records called blocks. Blocks can hold transactions, documents, files or any data you like, really, but the important thing is that blocks are chained together using hashes. The blockchain networks consists of interconnected nodes which update the blocks together using a consensus algorithm (like proof-of-work). 

Original source: [hackernoon](https://hackernoon.com/learn-blockchains-by-building-one-117428612f46)

## Tools

* Python 3.6+
* Python IDE
* HTTP client (Postman or cURL)
* Flask and Requests Library for Python

## Installation

Go to [Python](https://www.python.org/downloads/) and download “Python 
3.6” (the x86 “executable installer” version). Install it.

Install the “Flask” library using the command: 
```bash
pip3 install Flask==0.12.2 requests==2.18.4
```
Go to [Postman](https://www.getpostman.com), download and install it

## Synchronization

Once the application is fully set-up, you can grab a different machine if you like and spin up different nodes on your network. Or spin up processes using different ports on the same machine.

* It is easier to spin up another node on your machine, on a different port, and register it with your current node (using -p or --port switches and then the port number). 
* Thus, you will have two nodes:  http://localhost:5000 and http://localhost:5001. 
 
## Interacting with the Blockchain 

1.	Now open command shell and go to your project file directory. 
2.	Start your first blockchain node by running the command: 
```bash
python3 blockchain.py 
```
If everything is OK you will see the following result: 
```bash
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit) 
```
3.	Now open Postman. 
4.	Mine a block by making a GET request to http://localhost:5000/mine.
5.  Create a new transaction by making a POST request to http://localhost:5000/transactions/new with a body containing our transaction JSON structure.
6.  Inspect the full chain by requesting http://localhost:5000/chain. 
7.  Register a new node by making a POST request to http://localhost:5000/nodes/register. Do not forget to run another node with port 5001 on your machine.
8.  Finally, resolve chain-length conflicts by making a GET request to http://localhost:5000/nodes/resolve, thus determing the authoritative chain.

### Module
MI1: Module 2: E1
