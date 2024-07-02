# CREATE A TOKEN

This Solidity program is a simple 'CREATE A TOKEN' program which demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to make familiar to the one's who are new to Solidity and teaches how it works.

## Description

This program code is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The Solidity code provided defines a smart contract named MyToken. This program serves as a simple and straight forward introduction to Solidity programming, and can be used as a development for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier:MIT
pragma solidity 0.8.26;

contract MyToken
{
    string public tokenName="BITCOIN";
    string public tokenAbbrv="BTC";
    uint public totalSupply=0;

    mapping (address=> uint) public currentBalance;

    function mint(address _address,uint _value)public
    {
        totalSupply+=_value;
        currentBalance[_address] +=_value;
    } 

    function burn(address _address, uint _value)public
    {
        if(currentBalance[_address] >= _value)
        {
            totalSupply -= _value;
            currentBalance[_address] -= _value;
        }
    }
}


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the respective "mint" and "burn" function.Finally, click on the "transact" button to execute the function and check your currentBalance.

## Authors

Name = Harroop Singh
Email-id = harroopghuman9537@gmail.com
