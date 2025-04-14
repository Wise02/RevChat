**Rev-Chat: A Chatroom Reverse Shell**

Real-time Flask chatroom with user authentication, message history, and optional file delivery — ideal for learning reverse shell and C2-style communication.

---

# RevChat

## 🔍 Overview
RevChat is a Flask-based real-time chatroom designed for learning and simulating reverse shell communication concepts. It supports user authentication, secure password storage, message broadcasting, and even includes an optional file delivery system to mimic payload distribution in red-team scenarios.

## ✨ Features

- 🔐 **User Authentication**
  - Login and signup pages with session management
  - Passwords hashed using Werkzeug
  - IP banning on brute-force attempts (in `server.py`)

- 💬 **Real-Time Chatroom**
  - Flask-SocketIO with Eventlet for asynchronous messaging
  - Broadcasts messages to all connected users
  - Sends chat history to new connections

- 💾 **File Delivery (Optional)**
  - `server.py` serves `driver.exe` after login, simulating payload access
  - HTML download interface included

- 🧠 **Pentesting-Lab Friendly**
  - Built for ethical hacking labs or secure internal testing

---

## 📁 File Structure

```
RevChat/
├── revchat.py           # Full app with Flask-Login and SQLite database
├── server.py            # Lighter version with memory-only user tracking & IP ban
├── requirements.txt     # All dependencies listed here
├── banned_ips.txt       # Auto-generated for IP banning (optional)
├── driver.exe           # Optional file for test delivery
└── templates/           # HTML UI templates
    ├── login.html
    ├── signup.html
    ├── chat.html
    └── driver.html
```

---

## 🚀 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/RevChat.git
cd RevChat
```

### 2. Create Virtual Environment (Optional but Recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the App

#### 1. BACKEND - this will handle all logic, connections and local files
```bash
python revchat.py
```
- Runs on `http://0.0.0.0:87`
- Requires templates and creates `users.db`

#### 2. FRONTEND - this will handle the interface, HTML pages, IPs, and more.
```bash
python server.py
```
- Runs on `http://0.0.0.0:80`
- Requires `driver.exe` in root folder

---

## 🛡️ Legal

**For educational use only.** Do not deploy or test this software on unauthorized systems or networks.

---

## 📜 License

MIT License – use it freely with credit.
