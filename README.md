# Project Title

The "MyToken" smart contract is a fundamental example of a cryptocurrency token in Solidity. It showcases the essential features of token creation, including minting to increase the total supply and user balances, and burning to reduce the total supply while maintaining balance integrity. This contract is an excellent starting point for those exploring token development in Solidity.

## Description

This project consists of a simple Ethereum smart contract written in Solidity. The contract represents a basic cryptocurrency token and includes functionality for minting and burning tokens. Additionally, it stores token details such as the token name, abbreviation, and total supply.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public Token_Name = "Tobias";
    string public Token_Abbrv = "Toby";
    uint public TotalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address_, uint _coin) public {
        TotalSupply += _coin;
        balances[_address_] += _coin;
    }

    // burn function
    function burn (address _address_, uint _coin) public {
        if (balances[_address_] >= _coin){
           TotalSupply -= _coin;
           balances[_address_] -= _coin; 
        }
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18", and then click on the "Compile SolidityProject.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Next is click on "Deploy" and go to "Deployed Contracts" and run the code first copy "Account" and paste it on the address so when minting and burning the token it will diplay it.

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Juan Alfonso Q. Magpantay
@Alfie__004


## License

This project is licensed under the Juan Alfonso Q. Magpantay License - see the LICENSE.md file for details
