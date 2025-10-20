// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract OwnerOnlyContract {
    address public owner;

    constructor() {
        owner = msg.sender; // Владелец — адрес, который разворачивает контракт
    }

    modifier onlyOwner() {
        require(msg.sender == owner, "Not the contract owner");
        _;
    }

    // Пример функции, доступной только владельцу
    function doOwnerTask() external onlyOwner {
        // логика, доступная только владельцу
    }

    // Возможность смены владельца
    function transferOwnership(address newOwner) external onlyOwner {
        require(newOwner != address(0), "Invalid address");
        owner = newOwner;
    }
}
