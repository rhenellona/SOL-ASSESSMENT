# Solidity Beginnner Course Assessment

Final project for the fullfillment of ETH PROOF: Beginner EVM Course.

## Description

In this project, we are asked to create our own tokens with the following requirements.

## Process
* So for the first requirement, my contract should have public variables that store the details about my coin (Token Name, Token Abbrv., Total Supply)

```sol 
contract MyToken {

    string public TokenName = "BRAVE";
    string public TokenAbbrv = "BRVE";
    uint public totalSupply = 0;
```    
In here, I used string, set it on public so it can be accessible to join this blockchain. 
For the total supply, I used uint (unsigned integer) since there should be no negative number in this project. 

* Second requirement, my contract should have a mapping of addresses to balances (address => uint)

``` blue
  mapping (address => uint) public balances;
```
In here, we used mapping, address to uint and make it public. The purpose of this process is when an addresss pass into here, its gonna return
the token amount that the address contains. 






### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```
code blocks for commands
```

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
