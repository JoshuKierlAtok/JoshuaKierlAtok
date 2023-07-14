# Atok

# Description

# Getting Started
So to try run this program here in https://remix.ethereum.org/. in here you can run this code. Add file then paste this code that I created
      contract MyToken {
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
