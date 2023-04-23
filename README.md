# MyToken

The "MyToken" project in Solidity serves as an example of the programming language's important syntax and features. The goal of this project is to give individuals who are unfamiliar with Solidity a place to start learning about it.


## Description

Written in Solidity, a programming language for creating smart contracts for the Ethereum blockchain, this program is a simple contract. A single function in the contract returns the string "MyToken" This project acts as an easy-to-understand lesson on Solidity programming and can be used as a platform for following deeper projects.

## Getting Started

### Executing program

To run this project, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Janna.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
string public TokenName = "Janna";
string public TokenAbbrv = "JN";
uint public  TotalSupply = 0;

    /// mapping variable here
    mapping(address => uint) public balances;
     
// mint function
    function mint (address _address, uint _value) public {
       TotalSupply += _value;
       balances[_address] += _value;
    }
    
// burn function
    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
          TotalSupply -= _value;
          balances[_address] -= _value;
       }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile janna.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

## Authors

Janna Isabel Galvez

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
