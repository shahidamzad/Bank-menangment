# Bank Management — Simple CLI & Streamlit App 🏦

A small, educational bank account management system implemented in Python. It provides a CLI interface (`main.py`) and a simple Streamlit web UI (`app.py` using `hello.py` for business logic). Account data is persisted to `data.json`.

---

## ✅ Features

- Create an account (age >= 18 and 4-digit PIN required)
- Deposit and withdraw money (deposit limited to 1–10000)
- View account details
- Update name/email/PIN
- Delete an account
- Data persisted to `data.json`

---

## 🔧 Requirements

- Python 3.8+
- Optional (for web UI): streamlit

Install Streamlit if you want the web interface:

```bash
pip install streamlit
```

---

## 🚀 Quick Start

1. (Optional) Create and activate a virtual environment:

```powershell
python -m venv venv
venv\Scripts\Activate.ps1    # PowerShell
# or
venv\Scripts\activate.bat     # cmd
```

2. Install Streamlit (only needed for the web UI):

```bash
pip install streamlit
```

3. Run the CLI interface:

```bash
python main.py
```

Follow the numbered prompts (create account, deposit, withdraw, etc.).

4. Run the Streamlit web UI:

```bash
streamlit run app.py
```

Open the local URL printed by Streamlit in your browser.

---

## 📁 Data

All accounts are stored in `data.json` at the project root. This file contains a JSON array of account objects such as:

```json
{
  "name": "Alice",
  "age": 30,
  "email": "alice@example.com",
  "pin": 1234,
  "accountNo.": "Ab1#2x",
  "balance": 0
}
```

> Note: PINs are stored in plaintext in `data.json` — this project is educational and not production-secure.

---

## 🧪 Using the library (programmatic)

You can also use the `hello.py` module programmatically. Example:

```python
from hello import Bank
user, msg = Bank.create_account('Bob', 25, 'bob@example.com', 4321)
print(msg)
```

---

## 💡 Improvements / TODO

- Hash PINs instead of saving plaintext
- Add unit tests and CI
- Add more input validation and better error handling
- Add pagination / search when many accounts exist

---

## 🤝 Contributing

Contributions welcome — open an issue or a PR with a short description of your change.

---

## 📜 License

This project is provided as-is for educational purposes. You may use or modify it under the terms of the MIT License.

---

If you'd like, I can also add a `requirements.txt`, examples, or a short CONTRIBUTING guide — tell me which you'd prefer. ✨
