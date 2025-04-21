# 💠 DECOtoken (ERC-20 Token Example)

This project is a practical exercise focused on implementing a basic ERC-20 token using Solidity. It is part of a blockchain development course and demonstrates how to create a fungible token on the Ethereum blockchain.

## 📌 Objective

To implement a smart contract that follows the [ERC-20](https://eips.ethereum.org/EIPS/eip-20) token standard, with core functionalities including:

- Token transfer between addresses
- Approval and delegated transfers (`approve` / `transferFrom`)
- Balance queries and total supply tracking

---

## 🔧 Token Specifications

| Property        | Value               |
|----------------|---------------------|
| Name           | DECO Coin           |
| Symbol         | DECO                |
| Decimals       | 18                  |
| Total Supply   | 10,000,000,000 DECO |

> The total supply is assigned to the deployer address upon contract deployment.

---

## 🧱 Project Structure

- `ERC20Interface` – Interface defining the standard ERC-20 methods.
- `DECOtoken` – Smart contract implementing:
  - `totalSupply()`
  - `balanceOf(address)`
  - `transfer(address, uint256)`
  - `approve(address, uint256)`
  - `transferFrom(address, address, uint256)`
  - `allowance(address, address)`

---

## ▶️ How to Test with Remix

1. Open the [Remix IDE](https://remix.ethereum.org/).
2. Create a new file and paste the content of `DECOtoken.sol`.
3. Compile using Solidity compiler version `0.8.7`.
4. Navigate to the **Deploy & Run Transactions** tab:
   - Environment: `JavaScript VM`
   - Click **Deploy**
5. After deployment:
   - Use `balanceOf` to check the deployer's token balance.
   - Use `transfer` to send tokens to another address.
   - Use `approve` and `transferFrom` to test delegated transfers.

---

## 🧪 Example Test

```solidity
// Address A (deployer) transfers 100 tokens to address B
transfer("0x1234...", 100 * 10**18);

// Address B approves address C to spend 50 tokens
approve("0x5678...", 50 * 10**18);

// Address C calls transferFrom to move 50 tokens from B to itself
transferFrom("0x1234...", "0x5678...", 50 * 10**18);
```

## Notes
 - This contract is intended for educational use only and should not be used in *production without proper auditing* .

 - It closely follows the ERC-20 standard to ensure compatibility with Ethereum tools and dApps.

## File: DECOtoken.sol

The full source code can be found in the `DECOtoken.sol` file.

