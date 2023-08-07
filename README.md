# ethavaxmod-1
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
