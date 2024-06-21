# ETH PROOF: Beginner EVM PROJECT

This Solidity program is a simple smartcontract "Token" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to know how the token is created in Solidity.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions that is used to mint and burn the number of tokens. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract MyToken {

    // public variables here
    string public Token_Name = "Eth Beginner project";
    string public Token_abbrv = "ETH";
    uint public Total_Supply = 0;

    // mapping variable here
    mapping(address => uint) public Token_balances;

    // mint function
    function mint (address _address, uint _value) public {
        Total_Supply += _value;
        Token_balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (Token_balances[_address] >= _value) {   
        Total_Supply -= _value;
        Token_balances[_address] -= _value;
        }
    }    
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "mint" or "burn" function and choose the address of the token. Finally, click on the "transact" button to execute the function and retrieve the number of tokens minted or burn.

## Authors

Metacrafter  jeffryanpol


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
