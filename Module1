// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract Votingmachine {
    address public owner;
    uint256 public votesinmachine;
    mapping(address => uint256) public votes;

    constructor() {
        owner = msg.sender;
        votesinmachine = 0;
    }

    function vote(uint256 numberOfVotes) public {
        // Use require to validate inputs or conditions
        require(numberOfVotes > 0, "Number of votes must be greater than zero.");

        // Use revert to handle custom error messages
        if (votes[msg.sender] + numberOfVotes > 250) {
            revert("You cannot cast more than 250  votes.");
        }

        // Use assert for internal errors that should never occur
        assert(votesinmachine + numberOfVotes >= votesinmachine);

        votes[msg.sender] += numberOfVotes;
        votesinmachine += numberOfVotes;
    }
  
}
