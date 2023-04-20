# Solidity Beginnner Course Assessment

Final project for the fullfillment of ETH PROOF: Beginner EVM Course.

## Description

In this project, we are asked to create our own tokens with the following requirements.

## Process
* So for the first requirement, my contract should have public variables that store the details about my coin (Token Name, Token Abbrv., Total Supply)

```solidity
contract MyToken {

    string public TokenName = "BRAVE";
    string public TokenAbbrv = "BRVE";
    uint public totalSupply = 0;
```    
In here, I used string, set it on public so it can be accessible to join this blockchain. 
For the total supply, I used uint (unsigned integer) since there should be no negative number in this project. 

* Contract should have a mapping of addresses to balances (address => uint)

```solidity
  mapping (address => uint) public balances;
```
In here, we used mapping, address to uint and make it public. The purpose of this process is when an addresss pass into here, its gonna return
the token amount that the address contains. 

* Create a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount.

```solidity
 function mint (address _address, uint _value) public {
        totalSupply += _value; 
        balances[_address] += _value;
    }
```
In this, mint function is used to confine the address and value. The function increases the total supply by that number and increases
the balance of the address by the said amount. 
Used uint for value since we are avoiding having negative numbers. Increase total amount by using addition (+) = value. Do the same thing for balances
address and increase that balance by the value.

* Contract should have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.

* Burn function should have conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.
 In this, I used if statement, so if the balance of our address is greater than or equal to the given value, then we will take it from these.

```solidity
function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) { 
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```
For the burn function, we used subtraction (-) since its purpose is to destroy tokens. Use same code from the mint function BUT change (+) to (-). 

### NOTE

* Make sure that the balances are greater than or equal to the value that is being asked for, if its not then it will not execute and nothing will happen.

### Executing program

* Click the solidity compiler button on the left part of the screen, and click compile my token.
* Click the deploy & run transactions button under the solidity compiler button. On that panel, click deploy. Scroll down to the deployed contracts panel and expand. In this panel, we can see buttons of the variables that we created. Click each button to check if its working. 
* On the deploy & run transactions panel, look for the address and copy it. 
* On the deployed contracts panel, look for balances and paste address and click call. 
* For mint and burn, paste the address and enter desired value. After that, click again the call button on the balances and totalSupply button.
* Check if the program doesn't burn more than what you have. If the total supply and balance has not changed then the project is complete.

### NOTE

* Look for the green check in every transaction that you make, if you see a green check it means that the transaction went through.

## Authors

Rhene F. Llona
email : 8213812@ntc.edu.ph


## License

Unlicensed.
