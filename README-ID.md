🚀 Octra → Ethereum Bridge Script

Script Python untuk bridge OCT (Octra) ke wOCT (Ethereum) secara manual.

---

✨ Features

- Lock OCT di Octra
- Generate proof otomatis
- Claim wOCT di Ethereum
- Support auto-claim
- Single file (simple & portable)

---

⚙️ Requirements

- Python 3.10+
- pip / pip3
- ETH balance untuk gas

Install dependency:

pip install web3 requests eth-abi pynacl

---

🔐 Setup

Copy file env:

cp .env.example .env
nano .env

Isi ".env":

OCTRA_PRIVATE_KEY=YOUR_BASE64_PRIVATE_KEY
ETH_PRIVATE_KEY=0xYOUR_PRIVATE_KEY
BRIDGE_EVM_RECIPIENT=0xYOUR_ADDRESS

# Optional
ETH_RPC=https://ethereum-rpc.publicnode.com
OCTRA_RPC=https://octrascan.io/rpc

---

🚀 Usage

1. Lock OCT (Step 1)

python octra_bridge_woct.py --amount 1 --evm-recipient 0xYOUR_ADDRESS --lock-only --env-file .env

---

2. Check status

python octra_bridge_woct.py --tx TX_HASH --env-file .env

---

3. Claim (Mint wOCT)

python octra_bridge_woct.py --tx TX_HASH --send --env-file .env

---

⚡ Full Auto (Lock + Claim)

python octra_bridge_woct.py --amount 1 --evm-recipient 0xYOUR_ADDRESS --wait-header 1800 --send --env-file .env

---

🔥 Send All Balance

python octra_bridge_woct.py --all --evm-recipient 0xYOUR_ADDRESS --env-file .env

---

⚠️ Important Notes

- Jangan share private key
- Gunakan wallet khusus (bukan main wallet)
- Pastikan ETH cukup untuk gas
- Max decimal: 6

---

🔒 Security

- Private key digunakan hanya untuk signing lokal
- Tidak ada pengiriman private key ke server
- Semua transaksi dikirim dalam bentuk signed tx

---

📌 Disclaimer

Gunakan dengan risiko masing-masing.
Pastikan memahami cara kerja bridge sebelum menggunakan dana besar.

---

👤 Author

GitHub: https://github.com/robynasuro
