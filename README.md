# Hash Identifier

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/hash-id)

____

**hash-id** is a command line program for identifying **hash types** based on [Zion3R's implementation](https://github.com/blackploit/hash-identifier).   
This software is meant for enumeration, this is **not** a hash cracking tool, and it isn't definitive, the only way to be sure of the algorithm is after the hash has been reversed.    

## Usage
```
hash-id [OPTIONS]
```   

**Examples:**
  * Using a CLI argument
    ```
    $ hash-id -h fc7feb971470bd3d08d241f88db1ea38
    ```
  * Using a text file
    ```
    $ hash-id -f ./hashes.txt
    ```
  * Output: 
    ```
    $ hash-id -f ./hashes.txt -h fc7feb971470bd3d08d241f88db1ea38
    > Hash: b89eaac7e61417341b710b727768294d0e6a277b
    >   [+] SHA-1
    >   [+] MySQL5 - SHA-1(SHA-1($pass))
    >   [+] Tiger-160
    >   [+] Haval-160
    >   [+] RipeMD-160
    >  #(...)
    > ------------------------------------------
    > Hash: 2303b15bfa48c74a74758135a0df1201
    >    [+] MD5
    >    [+] Domain Cached Credentials - MD4(MD4(($pass)).(strtolower($username)))
    >    [+] RAdmin v2.x
    >    [+] NTLM
    >    [+] MD4 
    >  #(...)
    > ------------------------------------------
    >  #(...)
    ```
**Options**:    
| short | long     | type     | description                                 |
|-------|----------|----------|---------------------------------------------|
| `-f`  | `--file` | FILE     | File containing hashes (each one in a line) |
| `-h`  | `--hash` | STRING   | Hash value to be identified                 |

**Flags**:    
| short | long        | description                 |
|-------|-------------|-----------------------------|
|       | `--help`    | Prints help information     |
| `-V`  | `--version` | Prints version information  |

**Info**:   
  * Algorithms are displayed in order of probability, so you should start testing by the first. 
  * A hash argument and a file can be used at the same time.

## Install
Currently, just a snap package is suported. If you want to maintain a distro specific package, please check the [contributing](##Contributing) section.
  * Snap
    ```
    sudo snap install hash-id --beta
    ```

## Contributing
Thank you for wanting to contribute to this project! Here are some ways you can help:
  * Translating this documentation to your language
  * Creating documentation
  * Refactoring code (PRs are always welcome)
  * Adding more functionality    

Always before starting to work on something, check the [issues](https://github.com/Tashima42/hash-id-rust/issues) to see if anyone else is working on the same thing, if anyone is working and you want to start, please create an issue and let me know. Code changing PRs without an issue will not be accepted.
