Abi -> Rest Converter
Author: Dennis Mckinnon

This is a small tool (for mostly my own purposes) which takes an abi file and produces rest endpoint snippets which can then be inserted into a proper node server.

Some assumptions I make:
You are using restify
You are using eris-contracts as erisC
Your contract object is named "contract" 
You are server object is named "server" (if its not you just need to change the server.get(...) lines)

The flow of using this is to write a contract, compile using solc, use abircon to convert to a .rest file with the rest endpoints, copy the endpoints into your node server along with the functions.

This might not be the best code but its several hundred lines you didn't have to write (and update every time you change the contract)

Usage:

`abircon /path/to/inputfile.abi`

or if not on your PATH and executable

`python /path/to/abicon/ /path/to/inputfile.abi`

will output to `inputfile.rest` 