# LOAN_ACCOUNT Smart Contract

# Overview

The `LOAN_ACCOUNT` smart contract is a basic loan management system written in Solidity. It allows the contract owner to manage a loan amount by increasing, decreasing, and setting new loan values. 

# Prerequisites

Basic understanding of Solidity.
An Ethereum wallet (e.g., MetaMask).
Ethereum development environment (e.g., Remix, Truffle, Hardhat).

# Contract Details

# State Variables

 `address public owner`: The address of the contract owner.
 `uint256 public loan`: The current loan amount, initialized to 5000 units.

# Constructor

- `constructor()`: Sets the `owner` to the address that deploys the contract.

# Functions

#`IterestRate(uint256 _peso)`

 Increases the loan amount by `_peso`.
 `_peso` must be greater than 50.

# `MonthlyPayment(uint256 _peso)`

 Decreases the loan amount by `_peso`.
 `_peso` must be greater than 20 and less than or equal to the current loan.

# `calculateNewLoan(uint256 _initialLoan, uint256 _additionalLoan)`

 Returns the new loan amount by adding `_additionalLoan` to `_initialLoan`.

# `calculateRemainingLoan(uint256 _initialLoan, uint256 _soldQuantity)`

 Returns the remaining loan amount by subtracting `_soldQuantity` from `_initialLoan`.
 `_soldQuantity` must be less than or equal to `_initialLoan`.

# `setLoan(uint256 newLoan)`

 Updates the loan amount to `newLoan`.
 Only the contract owner can call this function.

# Usage

 Deploy the Contract:
    Deploy using an Ethereum development environment like Remix.
    The deploying address becomes the contract owner.

Interact with the Contract:
    Use `IterestRate` and `MonthlyPayment` to modify the loan.
    Use `calculateNewLoan` and `calculateRemainingLoan` for calculations.
    Use `setLoan` to update the loan amount (owner only).

 # License

This project is licensed under the MIT License.
