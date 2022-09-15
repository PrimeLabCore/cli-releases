
### PrimeLab TPS-CLI
  


To run the PrimeLab TPS Testing CLI tool you will need a `client-id` and `start-key`. This will provide you with a private key and certificate to manage this client. You can get these from the PrimeLab team ([Here](https://primelab.io/contact/))


 ### Step 1:    Authenticate your CLI client with the network

    ./primechain init --client-id YOUR-CLIENT-ID --start-key YOUR-START-KEY
  
  **Important** - `client-id` and `start-key` are both non-transferrable keys and may not be used by more than one user.



 ### Step 2:    Create a PrimeLab Wallet

    ./primechain accounts create
  
**Important** - The  `accounts create` command will output your 12 word seed phrase as well as your pub/private key. We recommend saving your seed phrase in a secure location. 
 
 
 ### Step 3:    Execute TPS Test on PrimeLab TestNet
 
**Parameters** - The  `benchmark` command supports modifying parameters in order to test different types of transactions on the PrimeLab TestNet. You may modify the parameters to execute the TPS test to fit your specific use-case.

**Supported Transaction Types:**  
 1. createNFT
 2. createConnection
 3. generateFAK
 4. sendToken
 5. signContract

**Example CMD:**

    ./primechain benchmark --createNFT 10000 --createConnection 20000 --generateFAK 30000 --sendToken 40000 --signContract 50000

  
  

### Need Help?
  

```shell

$ ./primechain help

  

  _____           _                      _                _     
 |  __ \         (_)                    | |              | |    
 | |__) |  _ __   _   _ __ ___     ___  | |        __ _  | |__  
 |  ___/  | '__| | | | '_ ` _ \   / _ \ | |       / _` | | '_ \ 
 | |      | |    | | | | | | | | |  __/ | |____  | (_| | | |_) |
 |_|      |_|    |_| |_| |_| |_|  \___| |______|  \__,_| |_.__/ 
                                                                
                                                                
Primechain TPS Tool is a tool to test the performance of Primechain network.

Usage:
  tools [command]

Available Commands:
  accounts    Accounts commands
  benchmark   Benchmark the performance of PrimeChain
  completion  Generate the autocompletion script for the specified shell
  help        Help about any command
  init        Initialize Primechain CLI tool

Flags:
      --auth-server string   Authorization server address (default "traffic.cloudweb3.io")
  -h, --help                 help for tools
  -t, --toggle               Help message for toggle

Use "tools [command] --help" for more information about a command.
  

```
