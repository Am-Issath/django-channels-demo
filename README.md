# 💬 Real-Time Chat App using Django Channels

A blazing-fast WebSocket-based real-time chat application built with **Django**, **Channels**, and **Redis**. Connect multiple users to the same room and chat live! ⚡

![Django](https://img.shields.io/badge/Django-5.2-success?logo=django&logoColor=white)
![Channels](https://img.shields.io/badge/Channels-4.0-blue?logo=websocket)
![Redis](https://img.shields.io/badge/Redis-7.2.6-red?logo=redis&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)

---

## 🌐 Demo Preview

> 🖥️ Visit: `http://localhost:8000/chat/room1/`  
> You'll be prompted to enter a username and can chat live with others in the same room.

![Chat App Demo Screenshot](your-screenshot-url-if-available)

---

## 🚀 Features

- 🔌 Real-time WebSocket-based messaging
- 🧠 Username stored in browser using `localStorage`
- 🧵 Multiple rooms support (e.g., `/chat/room1/`, `/chat/room2/`)
- 🔒 Anonymous user fallback
- 💡 Built with modern Django + Channels stack

---

## 📁 Project Structure

```bash
django-channels-demo/
├── chat/
│   ├── templates/
│   │   └── room.html
│   ├── consumers.py
│   ├── routing.py
│   └── ...
├── myApp/
│   ├── settings.py
│   ├── asgi.py
│   └── urls.py
├── db.sqlite3
└── manage.py
└── requirements.txt
```

---

## 🔧 Tech Stack

- 🐍 Python 3.12	=> Backend language
- 🌐 Django 5.2	 => Web framework
- 🔌 Django-channels	=>WebSocket support
- 🧠 Redis	=> Pub/Sub layer for Channels
- 🎨 HTML + JS	=> Frontend

---

## 🛠️ Setup & Run Locally

### 1️⃣ Clone the Repo
```bash
git clone https://github.com/Am-Issath/django-channels-demo.git
cd django-channels-demo
```

### 2️⃣ Create & Activate Virtualenv (optional but recommended)
```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

> If you don’t have requirements.txt, install manually:

```bash
pip install django channels channels_redis
```
### 4️⃣ Run Redis Server (required)
> Ensure Redis is running:
```bash
redis-server
```
> Or install it:

- On macOS: brew install redis
- On Ubuntu: sudo apt install redis

### 5️⃣ Run the Development Server
```bash
daphne -p 8000 myApp.asgi:application
```
> You can also use python manage.py runserver but daphne is more production-accurate.

### 6️⃣ Open in Browser
```bash
http://127.0.0.1:8000/chat/room1/
```

---

## 🧪 How It Works

- A WebSocket connection is created on page load
- Messages are sent/received using Django Channels & Redis
- Chat room logic is isolated by room_name
- Anonymous users are prompted for a username via JS

## 📦 Dependencies
```
Django>=5.2
channels>=4.0
channels-redis>=4.1
redis>=4.5
```

## 🙌 Contribute

- Pull requests are welcome. Open an issue first to discuss what you’d like to change.

## 💡 Author

- Issath – ![GitHub](https://github.com/Am-Issath)