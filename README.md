# Solidity

This project is a starting point for beginners in understanding the implementation and working of functions along with creating a token.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. In this contract we have declared two functions which can mint and burn the tokens that we created into/from the balance and the total supply of the account. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ybu.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract MyToken {
    string public tokenname="YASHWANTH";
    string public tokenabbrv="YBU";
    uint public totalsupply=5000;
    mapping(address => uint)public balance;
    function mint(address mintaddr, uint  mintval)public {
      totalsupply += mintval;
      balance[mintaddr] += mintval;
   }
   function burn(address burnaddr, uint burnval)public {
      if(balance[burnaddr]>= burnval){
        totalsupply -= burnval;
        balance[burnaddr] -= burnval;
      }
     }
  }

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile ybu.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "ybu" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with the mint and burn functions to add or remove tokens from the balance of that account address respectively.

## Authors

Yashwanth BU
[@yashwanthbuu@gmail.com](https://twitter.com/metacraftersio)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
