# Project Title
For this project, write a smart contract that implements the require(), assert() and revert() statements.

Upload your solution to GitHub and share the link with us along with a quick code walk-through as explained below.



## Description

An in-depth paragraph about your project and overview of use.

## Getting Started

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

kushank chuhan

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)


## License

This project is licensed under the [KUSHANK CHAUHAN] License - see the LICENSE.md file for details


## code

pragma solidity ^0.8.0;

contract module1 {
    function errorhandle(uint256 x, uint256 y) public pure returns (uint256) {
        // Using require()
        require(x != 10, "x should not be ten");
        require(y != 20, "y should not be twenty");

        // Using assert()
        uint256 result = x - y;
        assert(result <= x && result <= y);

        // Using revert()
        if (x < y) {
            revert("x should be greater than or equal to y");
        }

        return result;
    }
}
