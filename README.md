🚀 Octra → Ethereum Bridge Script

A simple Python script to bridge OCT (Octra) to wOCT (Ethereum).

---

🌏 Documentation

- 🇬🇧 English: This README
- 🇮🇩 Indonesian: "README-ID.md" (./README-ID.md)

---

✨ Features

- Lock OCT on Octra
- Generate bridge proof automatically
- Claim wOCT on Ethereum
- Supports auto-claim mode
- Single-file script (easy to use)

---

⚙️ Requirements

- Python 3.10+
- pip / pip3
- ETH balance for gas fees

Git Clone

```
git clone https://github.com/robynasuro/octra-bridge.git
cd octra-bridge
```

Install dependencies:

```
pip install web3 requests eth-abi pynacl
```

---

🔐 Setup

Copy environment file:


```
cp .env.example .env
nano .env
```

Fill in your configuration:

```
OCTRA_PRIVATE_KEY=YOUR_BASE64_PRIVATE_KEY
ETH_PRIVATE_KEY=0xYOUR_PRIVATE_KEY
BRIDGE_EVM_RECIPIENT=0xYOUR_ADDRESS

# Optional
ETH_RPC=https://ethereum-rpc.publicnode.com
OCTRA_RPC=https://octrascan.io/rpc

OCTRA_BRIDGE_VAULT=oct5MrNfjiXFNRDLwsodn8Zm9hDKNGAYt3eQDCQ52bSpCHq
ETHEREUM_BRIDGE=0xE7eD69b852fd2a1406080B26A37e8E04e7dA4caE
OCTRA_LIGHT_CLIENT=0xC01cA57dc7f7C4B6f1B6b87B85D79e5ddf0dF55d
WOCT_TOKEN=0x4647e1fE715c9e23959022C2416C71867F5a6E80
```

---

🚀 Usage

1. Lock OCT (Step 1)

```
python octra_bridge_woct.py --amount 1 --evm-recipient 0xYOUR_ADDRESS --lock-only --env-file .env
```

---

2. Check status
```
python octra_bridge_woct.py --tx TX_HASH --env-file .env
```

---

3. Claim (Mint wOCT)
```
python octra_bridge_woct.py --tx TX_HASH --send --env-file .env
```
---

⚡ Full Auto (Lock + Claim)
```
python octra_bridge_woct.py --amount 1 --evm-recipient 0xYOUR_ADDRESS --wait-header 1800 --send --env-file .env
```
---

🔥 Send Full Balance
```
python octra_bridge_woct.py --all --evm-recipient 0xYOUR_ADDRESS --env-file .env
```
---

⚠️ Important Notes

- Never share your private keys
- Use a dedicated wallet (not your main wallet)
- Ensure you have enough ETH for gas fees
- Max decimal precision: 6

---

🔒 Security

- Private keys are used locally for signing only
- No private key data is sent externally
- Only signed transactions are broadcasted

---

📌 Disclaimer

Use at your own risk.
Make sure you understand how the bridge works before using large funds.

---

👤 Author

GitHub: https://github.com/robynasuro
