# 🏥 Clinic Call MVP

### iPhone Controlled Clinic Communication System

A lightweight communication system designed for a small clinic to allow **reception and the doctor to communicate quickly using an iPhone and laptop**.

The **iPhone acts as the controller**, while the **laptop receives and displays the call** in real time.

---

## 🔄 How the System Works

```text
📱 iPhone
Controller
   │
   │ Send Call
   ▼
🌐 Flask Server
   │
   │ Update
   ▼
💻 Laptop
Call Display
```

The iPhone sends a predefined call, and the laptop automatically updates its display.

### Available Calls

| Code  | Request             |
| ----- | ------------------- |
| **K** | Kabo — needs you    |
| **P** | Prescription needed |
| **H** | Help needed         |

The controller also provides a **Clear** function to remove the active call.

---

# 📸 Project Demonstration

The screenshots below document the complete communication flow between the iPhone and laptop.

## 1. iPhone — Controller

The iPhone provides the control interface used to send a clinic call.

**Add screenshot here:**

```text
screenshots/01-iphone-controller.png
```

![iPhone Controller](screenshots/01-iphone-controller.png)

---

## 2. Laptop — Waiting for Call

The laptop remains ready to receive an incoming request from the iPhone.

**Add screenshot here:**

```text
screenshots/02-laptop-waiting.png
```

![Laptop Waiting](screenshots/02-laptop-waiting.png)

---

## 3. iPhone — Call Sent

A request is selected and sent from the iPhone controller.

**Add screenshot here:**

```text
screenshots/03-iphone-call-sent.png
```

![iPhone Call Sent](screenshots/03-iphone-call-sent.png)

---

## 4. Laptop — Call Received

The laptop receives the request and displays the corresponding call.

**Add screenshot here:**

```text
screenshots/04-laptop-call-received.png
```

![Laptop Call Received](screenshots/04-laptop-call-received.png)

---

# 🛠️ Technology Stack

| Component     | Technology                  |
| ------------- | --------------------------- |
| Backend       | Python                      |
| Web Framework | Flask                       |
| Frontend      | HTML / CSS / JavaScript     |
| Communication | REST API                    |
| Network       | Local Network / USB Hotspot |

---

# 📁 Project Structure

```text
clinic_call_mvp/
│
├── app.py
├── launcher.py
│
├── web/
│   └── index.html
│
├── screenshots/
│   ├── 01-iphone-controller.png
│   ├── 02-laptop-waiting.png
│   ├── 03-iphone-call-sent.png
│   └── 04-laptop-call-received.png
│
└── README.md
```

**Put your screenshots inside the `screenshots` folder using the filenames shown above.**

---

# ▶️ Running the System

Start the Flask server:

```bash
python app.py
```

The laptop runs the server and displays incoming calls.

The iPhone connects to the laptop using the laptop's local IP address.

Example:

```text
http://172.20.10.8:5000
```

Both devices must be connected through the same network connection.

---

# 🔌 API Functions

The system uses a simple REST API:

```text
GET  /api/state
POST /api/call
POST /api/clear
```

`/api/call` sends the selected request, while `/api/state` allows the laptop display to receive the latest status.

---

# 🎯 Project Objective

The objective was to create a simple, practical communication tool that can be used in a small clinic environment without relying on an external cloud service.

The project demonstrates:

* Client-server communication
* REST API implementation
* Real time status updates
* Local network communication
* Mobile to computer interaction
* Practical problem solving

---

## ✅ Project Status

**Completed**

**Developer:** Kabo Sekoto
