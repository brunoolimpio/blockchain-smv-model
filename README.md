# Blockchain model checking

This is the repository of the SMV and Python codes of my master thesis, about model checking of a blockchain, the base technology of the cryptocurrencies like Bitcoin and others.
There are two main files:
* smv-code-compiler.py is a simple SMV code generator that receives (automatically or manually) the input parameters of a blockchain, which are the number of nodes, users,
transactions and blocks. The output is a file containing the SMV code related to the blockchain formal model to be checked.

* blockchain-model.smv is the blockchain formal model, wrote in SMV input language. The content of this file is copied to the file generated by the compiler to compose the parametrized blockchain formal model, ready to be verified.

## Executing the compiler

The compiler is just a Python 3 file, so you only need to have this version of Python installed to open the file and run.

## Executing the blockchain formal model using nuXmv

1. Install the nuXmv. You can download it at: https://nuxmv.fbk.eu/index.php?n=Download.Download. You must fill a simple registration. Once installed, in general the executable file is inside the folder "bin". On Windows operating systems, the path will probably be "C:\Program Files (x86)\nuXmv-1.1.1-win64\bin"

3. Open the executable folder. On windows type cd "C:\Program Files (x86)\nuXmv-1.1.1-win64\bin"

4. Type: nuXmv.exe -int "PATH_TO_THE_SMV_FILE\blockchain.smv". This command will execute the nuXmv in interactive mode and load the file "blockchain.smv"

4. Type: go_msat; msat_pick_state; msat_simulate -v;build_model;
This group of commands will build the model and use the algorithm MSAT to  simulate the blockchain formal model.

5. If you want to proceed some CTL verification, there are two options at the end of the file blockchain.smv. Just uncomment one and type: check_ctlspec;
