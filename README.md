# ODMO Discord Bot

A modular, secure, and efficient Discord bot built with Python using the discord.py framework. This bot supports the Open Digimon Masters Online (ODMO) project by providing user account management features such as registration, deletion, password changes, and more — all backed by an SQL Server database.

This bot is developed to assist and enhance the experience of the Open Digimon Masters Online (ODMO) project from [Tenshimaru’s OpenDigimonMastersOnline GitHub repository](https://github.com/Tenshimaru/OpenDigimonMastersOnline).

---

## ✨ Features

- 🔐 Secure account registration via DM
- ❌ Account deletion with confirmation and password check
- 🔁 Password change using Discord identity
- 🆔 Reset secondary password securely
- 📧 View registered username and email
- 💾 MSSQL backend integration
- 🧩 Modular architecture using Cogs

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/odmo-discord-bot.git
cd odmo-discord-bot
```

### 2. Set up Python environment

It's recommended to use a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure your environment variables

Create a `.env` file in the root directory with:

```bash
copy .env.template .env
```
Add your bot token and Database connectin string:

```env
DISCORD_TOKEN=your-discord-bot-token-here
```

Change the CONN_STR Information to your needs.

```env
CONN_STR=Driver={SQL Server};Server=localhost\SQLEXPRESS;Database=DMOX;UID=sa;PWD=Your-Password;TrustServerCertificate=yes;
```

**⚠️ Keep this file secret!** It is already ignored in `.gitignore`.

### 5. Run the bot

```bash
python bot.py
```

The bot will automatically load all cogs from the `cogs/` directory.

---

## 🗃️ Project Structure

```
odmo-discord-bot/
│
├── bot.py               # Main bot entry point
├── .env                 # Environment variables (not tracked in Git)
├── requirements.txt     # Dependencies
├── cogs/                # Modular bot commands
│   ├── register.py
│   ├── deleteaccount.py
│   ├── changepassword.py
│   ├── resetsecondpassword.py
│   ├── username.py
│   └── email.py
├── db/
│   └── database.py      # MSSQL connection logic
└── README.md
```

---

## 🧠 Tech Stack

- Python 3.10+
- [discord.py](https://github.com/Rapptz/discord.py)
- Microsoft SQL Server
- python-dotenv

---

## 🛡️ Security Notes

- All sensitive actions (like delete or change password) are DM-only.
- Discord user ID is used for account authentication.
- Secrets like your token are never hardcoded (use `.env`).

---

## 🧑‍💻 Contributions

Pull requests are welcome. Please open an issue first to discuss what you would like to change.

---

## 📄 License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE.txt](https://github.com/Shadoukita/ODMO-Discord-Bot/blob/main/LICENSE.txt) file for details.

---

## 💬 Contact

For questions or support, open an issue on the repository or reach out via [Discord](https://discord.gg/VcNuqrW3WH).
