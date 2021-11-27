// SPDX-License-Identifier: GPL-3.0
pragma solidity ^0.8.10;

contract SimpleStorage {

    //this is a comment. This initializes to 0
    uint256 public favoriteNumber;

    struct People {
        uint256 favoriteNumber;
        string name;
    }

    People[] public people;

    mapping(string => uint256) public nameToFavoriteNumber;
    mapping(uint256 => string) public favNumtoName;

    function store(uint256 _favoriteNumber) public {
        favoriteNumber = _favoriteNumber;
    }

    //view, pure
    //reading things off of the block chain doesn't cost transaction fees
    function retrieve() public view returns(uint256) {
        return favoriteNumber;

    }

    //memory or storage are the two options
    //storage will persist after 
    function addPerson(string memory _name, uint256 _favoriteNumber) public {
        people.push(People(_favoriteNumber, _name));
        nameToFavoriteNumber[_name] = _favoriteNumber;
        favNumtoName[_favoriteNumber] = _name;
    }
}

