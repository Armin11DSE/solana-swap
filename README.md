# 🔄 Solana Swap Program

A Solana smart contract (Anchor-based) for swapping tokens between two parties using associated token accounts and a vault mechanism. The swap is executed in two steps: an offer is made by one user (the maker), and accepted by another (the taker).

---

## 🛠️ Build and Test

### 📦 Build the program

```bash
anchor build
```

This compiles the Solana program and generates the necessary IDL files.

### ✅ Run tests

```bash
anchor test
```

Runs the test suite located in the `tests/` folder, which:

- Mints test SPL tokens for two users (Alice and Bob)
- Simulates making an offer to swap tokens
- Simulates taking that offer and asserting the token transfers occurred correctly

---

## 🧾 Program Structure

- `makeOffer`: Maker locks offered tokens in a vault
- `takeOffer`: Taker sends desired tokens to the maker, receives the vault tokens
- Vault is closed and cleaned up after swap

---

## Credits

Based on [Solana Developer Bootcamp 2024 - Learn Blockchain and Full Stack Web3 Development - Projects 1-9](https://www.youtube.com/watch?v=amAq-WHAFs8)
