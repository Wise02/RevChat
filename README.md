**Rev-Chat: A Chatroom Reverse Shell**

A real-time Flask chatroom with user authentication, secure password handling, and Socket.IO-based messaging—ideal for learning reverse shell concepts in a safe, interactive environment.

---

## Overview

This project is a real-time chatroom application built with Flask, designed to simulate reverse shell interactions. It incorporates user authentication, secure password storage, and real-time messaging using Flask-SocketIO. Ideal for cybersecurity enthusiasts looking to explore reverse shell concepts in a controlled setting.

## Features

- **User Authentication**: Secure signup and login using Flask-Login and hashed passwords with Werkzeug.
- **Real-Time Messaging**: Instant communication facilitated by Flask-SocketIO and Eventlet.
- **Persistent Chat History**: Maintains a history of messages for new connections.
- **Database Integration**: Utilizes SQLite with SQLAlchemy for efficient data management.
- **Web Interface**: Clean and intuitive HTML templates for login, signup, and chat functionalities.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/chatroom-reverse-shell.git
   cd chatroom-reverse-shell
   ```

2. **Create a Virtual Environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**:
   ```bash
   python app.py
   ```
   The application will be accessible at `http://localhost:87` (you can change the IP and PORT in the `.py` file).

## Usage

- Navigate to `http://localhost:87` in your web browser.
- Register a new account or log in with existing credentials.
- Access the chatroom to start real-time messaging.

## Project Structure

```
chatroom-reverse-shell/
├── app.py
├── requirements.txt
├── templates/
│   ├── login.html
│   ├── signup.html
│   └── chat.html
└── README.md
```

## Dependencies

- Flask
- Flask-SocketIO
- Flask-Login
- Flask-SQLAlchemy
- Eventlet
- Werkzeug

Ensure all dependencies are listed in your `requirements.txt` file.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
