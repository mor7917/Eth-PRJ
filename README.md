# Eth-PRJ 
In this Project we to to create a program with the help of which we can mint or burn the token from the given account And for this we will use Remix Online IDE . And Here we are writing our project in the Solidity Language (.sol) is file extension for this

## Description 
   REQUIREMENTS
  *  Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply) .
  *  Your contract will have a mapping of addresses to balances (address => uint).
  * You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount .
  * Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
  * Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.

## Getting Started

### Executing Program

To run this Program we will use Remix Online compiler  https://remix.ethereum.org/ .

```javascript
pragma solidity 0.8.18;

contract MyToken {

   
   string public tokenName = "ETEH";
   string public tokenAbbrv = "ETH";
   uint public  totalSupply = 0;

    
   mapping(address => uint) public balances ;

   
   function mint(address _address, uint _value)public{
      totalSupply += _value;
      balances[_address] += _value;
   }

    
   function burn(address _address, uint _value)public{ 
      if(balances[_address]>= _value){
      totalSupply -= _value;
      balances[_address] -= _value;
      }
   }
}
```
## Author 

Ankit Mor
