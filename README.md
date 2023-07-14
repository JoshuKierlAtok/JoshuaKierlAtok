# Atok
The provided code represents a smart contract called "MyToken" written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract defines a custom token called "ATOK" with the symbol "ATK".
# Description
The provided Solidity program represents a basic implementation of a token contract called "MyToken." This contract allows the creation and management of a custom token named "ATOK" (abbreviated as "ATK") on the Ethereum blockchain.
# Getting Started
So to try run this program here in https://remix.ethereum.org/. in here you can run this code. Add file then paste this code that I created
     
contract MyToken {

   //  public variables here
    string public name = "ATOK";
    string public symbol = "ATK";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _amount) public {
        totalSupply += _amount;
        balances[_address] += _amount;
    }

    // burn function
    function burn(address _address, uint _amount) public {
        if(balances[_address] >= _amount) {
        totalSupply -= _amount;
        balances[_address] -= _amount;
    }
    }
}

Make sure that the Solidity Compiler is selected on the Remix interface. You can choose the appropriate compiler version by clicking on the "Compiler" tab in the right-hand panel and selecting a version that is compatible with your code.

Compile the contract by clicking on the "Compile" button in the Remix interface. You should see the compiler output in the right-hand panel, and any errors or warnings will be displayed if present.

Once the contract is successfully compiled, click on the "Deploy & Run Transactions" tab in the right-hand panel.

Click on the "Deploy" button to deploy the contract to the selected environment. This will create an instance of the contract on the blockchain.

After the contract is deployed, you will see the deployed contract details in the right-hand panel. You can interact with the contract using its functions and view its state variables.

To execute the functions, such as mint and burn, input the required parameters (e.g., _address and _amount) and click the corresponding button to execute the function.

# Author 
Joshua Kierl Atok

BSIT 2.1

#Lincese
This project is licensed under the MIT License - see the LICENSE.md file for details.
