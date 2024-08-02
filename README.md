# MyToken Smart Contract

## Overview
`MyToken` is a basic ERC20 token smart contract implemented using Solidity. This contract features standard ERC20 functionalities such as transferring tokens, allowing and transferring tokens on behalf of others, and minting new tokens. It also includes administrative features controlled by the contract owner.

## Features

- **ERC20 Standard Compliance**: Implements basic token functionalities including transfer, allowance, and balance checks.
- **Owner Privileges**: Only the owner can mint new tokens.
- **Events**: Emits events for transfers and approvals which assist in tracking changes on-chain.

## Contract Specifications

- **Solidity Version**: ^0.8.18
- **License**: MIT

### Functions

#### View Functions

- `totalSupply()`: Returns the total token supply.
- `decimals()`: Returns the number of decimals the token uses.
- `balanceOf(address account)`: Returns the token balance of a specific account.
- `allowance(address owner, address spender)`: Returns the remaining number of tokens that `spender` will be allowed to spend on behalf of `owner`.

#### Transaction Functions

- `transfer(address to, uint256 amount)`: Transfers `amount` of tokens to address `to`, and requires the sender has a sufficient balance.
- `approve(address spender, uint256 amount)`: Sets `amount` as the allowance of `spender` over the caller’s tokens.
- `transferFrom(address from, address to, uint256 amount)`: Transfers `amount` of tokens from address `from` to address `to`, using the allowance mechanism. `amount` is then deducted from the caller’s allowance.

#### Owner-Only Functions

- `mint(address to, uint256 amount)`: Mints `amount` of tokens and assigns them to `to`, increasing the total supply.

### Modifiers

- `onlyOwner`: Ensures that only the owner of the contract can execute the function.

## Events

- `Transfer(address indexed from, address indexed to, uint256 value)`: Emitted when `value` tokens are moved from one account (`from`) to another (`to`).
- `Approval(address indexed owner, address indexed spender, uint256 value)`: Emitted when `owner` approves `spender` to use `value` tokens on their behalf.

## Development and Testing

### Prerequisites

- [Node.js](https://nodejs.org/)
-hardhart/foundry/remix

### Setup and Deployment

1. Clone the repository:
2. Install dependencies:
3. Compile the smart contract:
4. Deploy the contract to a local test network:
