# My_Token
Token Creation
This solidity program is used to create our own token with the help of basic functions and conditional statements studied in the solidity programming.

Description
This program is a simple contract written in solidity. The contract has three public variables that store the details about the coin. Mapping is used to map an address with a value. This contract contains two functions mint and burn. Mint function is used to increase the totalSupply of our coin and in contrast burn function is used to destroy token.

Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "GOOGLE";
    string public tokenAbbrv = "GGL";
    uint public totalSupply = 12;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint (address _address , uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address , uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Assessment.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Assessment" contract from the dropdown menu, and then click on the "Deploy" button.

once the contract is deployed, you can interact with it by calling the mint function. Click on MyToken contract and select mint function. Provide adress and value to the mint function and click on transact to execute the function.

To check to supply of your token click on the public variables totalSupply in the contract section. It will display you the amount of token you minted.

Similarly, you can use the burn function and check the value by clicking on the ublic variable totalSupply.

Authors
Satyendra 22mca20969@cuchd.in

License
This project is licensed under the MIT License - see the LICENSE.md file for details
