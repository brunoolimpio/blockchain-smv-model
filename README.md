# Blockchain model checking

This is the repository of the SMV and Python codes of my master tesis, about model checking of the blockchain, the base technology of the cryptocurrencies like Bitcoin and others.
There are two main files:
* smv-code-generator.py is a simple SMV code generator that receives (automatically or manually) the input parameters of a blockchain, which are the number of nodes, users,
transactions and blocks. The output is the SMV code related to the MODULE main, mandatory to execute SMV codes and is responsible for the "instantiation" of the blockchain formal 
model to be checked.

* blockchain.smv is the blockchain formal model, wrote in SMV input language. 
