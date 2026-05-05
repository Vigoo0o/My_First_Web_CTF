# 🚩 Web Exploitation CTF — Authentication Challenge

A beginner-friendly **Capture The Flag** challenge focused on **Web Exploitation**, specifically targeting authentication systems, session management, and access control vulnerabilities.

Built as a hands-on learning project while studying cybersecurity on **TryHackMe**.

---

## 🎯 Challenge Goal

Find the hidden flag by exploiting weaknesses in the authentication and authorization system.

**Flag format:** `MSHN{XXXX}`

---

## 🧩 Vulnerability Categories

| # | Category | Difficulty |
|---|----------|------------|
| 1 | SQL Injection — Login Bypass | 🟢 Easy |
| 2 | Broken Access Control | 🟡 Medium |
| 3 | Directory Enumeration | 🟡 Medium |
| 4 | Cryptography — Flag Decoding | 🟢 Easy |

---

## 🗂️ Project Structure

```
Rigistration_System/
├── index.php             # Login page
├── login_process.php     # Authentication logic
├── dashboard.php         # User dashboard (requires login)
├── secret.php            # Admin-only secret page
├── logout.php            # Session destruction
├── connection.php        # Database connection + auto-setup
├── style/
│   └── main.css          # Stylesheet
└── Upload/
    ├── .htaccess         # Access control
    └── hidden.txt        # Hidden flag file
```

---

## ⚙️ Setup & Installation

### Requirements
- XAMPP (Apache + MySQL + PHP)
- Any OS: Windows / Linux / Mac

### Steps

**1. Install XAMPP**
Download from [apachefriends.org](https://www.apachefriends.org)

**2. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/ctf-auth-challenge.git
```

**3. Copy to web root**

| OS | Web Root |
|----|----------|
| Windows | `C:\xampp\htdocs\` |
| Linux | `/opt/lampp/htdocs/` |
| Mac | `/Applications/XAMPP/htdocs/` |

**4. Start XAMPP**
- Start **Apache** and **MySQL** from the XAMPP Control Panel

**5. Open in browser**
```
http://localhost/Rigistration_System/
```

> The database, tables, and default users are created **automatically** on first run — no manual SQL needed!

---

## 🔐 Default Credentials

> ⚠️ Knowing these is not enough — you still need to find the flag!

| Role | Username | Password |
|------|----------|----------|
| Normal User | `user` | `user123` |
| Admin | *(find it)* | *(find it)* |

---

## 💡 Hints

<details>
<summary>Hint 1 — Getting Started</summary>
Look carefully at how the login form processes your input...
</details>

<details>
<summary>Hint 2 — Privilege Escalation</summary>
Can you become someone you're not? Think about what controls access levels.
</details>

<details>
<summary>Hint 3 — Finding the Flag</summary>
The secret page hints at a hidden file. Can you reach it as the right user?
</details>

<details>
<summary>Hint 4 — Decoding</summary>
The flag is encoded. ROT13 is a classic cipher — try decoding it.
</details>

---

## 🛠️ Tech Stack

- **PHP** — Backend logic & session management
- **MySQL** — User database via PDO
- **HTML/CSS** — Frontend
- **Apache (.htaccess)** — File access control

---

## 📚 Learning Resources

- [TryHackMe](https://tryhackme.com) — Where this project was inspired
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) — Web vulnerabilities reference
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — SQL Injection labs

---

## ⚠️ Disclaimer

This project is built **intentionally vulnerable** for educational purposes only.
Do **not** deploy this on a public server. For local/CTF use only.

---

## 👤 Author

Built with 💻 as part of a cybersecurity learning journey on TryHackMe.

---

## 📄 License

MIT License — free to use for learning and CTF purposes.
