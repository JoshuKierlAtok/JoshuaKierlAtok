# Atok
The provided code represents a smart contract called "MyToken" written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract defines a custom token called "ATOK" with the symbol "ATK".
# Description
The provided Solidity program represents a basic implementation of a token contract called "MyToken." This contract allows the creation and management of a custom token named "ATOK" (abbreviated as "ATK") on the Ethereum blockchain.
# Getting Started
So to try run this program here in https://remix.ethereum.org/. in here you can run this code. Add file then paste this code that I created
     
      contract MyToken  {
     // public variables here
   
      string public name = "ATOK";
      
      string public symbol = "ATK";
      
      uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
       }
       }
     }
turo mo step by step paano mapapagana
# Author 
Joshua Kierl Atok

BSIT 2.1

