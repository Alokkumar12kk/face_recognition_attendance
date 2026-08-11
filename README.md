<h1 align="center">Face Recognition Attendance System 🎯</h1>

<p align="center">
  Automated, real-time attendance marking using OpenCV, dlib, and face-recognition — 90%+ accuracy, 70% less manual effort.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-3.1.3-092E20?style=flat-square&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenCV-4.4.0-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />
  <img src="https://img.shields.io/badge/dlib-19.21.0-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/face--recognition-1.3.0-black?style=flat-square" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" />
</p>

---

## 📌 Overview

The **Face Recognition Attendance System** replaces manual roll calls with an automated, camera-based pipeline built on Django. It detects and recognizes faces in real time using OpenCV, dlib, and the `face-recognition` library, logs attendance automatically, and surfaces everything through a live dashboard — cutting manual attendance effort by **70%** while maintaining **90%+ recognition accuracy** under real-world conditions.

---

## ✨ Features

- 🎥 **Real-time face detection & recognition** via webcam scanner
- ✅ **90%+ accuracy** across varied lighting and angles
- ⚡ **Automated attendance logging** — no manual entry required
- 📊 **Live dashboard** with Present / Employee Details / Attendance tabs
- 🗂️ **Per-profile attendance history** with timestamped entries
- 🔄 **One-click Reset & Refresh** controls on the dashboard
- 🔐 **Django admin panel** for managing employee profiles and records

---

## 🖼️ Dashboard Preview

**Present tab** — live scanner status and real-time presence table:

![Present tab dashboard](face_recognition_attendance/static/img
/bio.jpg)

**Attendance tab** — full attendance log with profile ID and timestamp:

![Attendance tab dashboard](face_recognition_attendance/static/img
/digital.jpg)

---

## 🛠️ Tech Stack

| Layer               | Technology                  |
|----------------------|------------------------------|
| Language             | Python 3.7+                  |
| Web Framework        | Django 3.1.3                 |
| Face Detection/Recog | OpenCV 4.4.0, dlib 19.21.0, face-recognition 1.3.0 |
| Image Processing     | Pillow 8.0.1, numpy 1.19.3   |
| Build Tool           | CMake 3.18.4                 |
| Alerts               | playsound 1.2.2              |
| Database             | SQLite (Django default)      |

**Full dependency list** (`req.txt`):
```
asgiref==3.3.1
click==7.1.2
cmake==3.18.4.post1
Django==3.1.3
dlib==19.21.0
face-recognition==1.3.0
face-recognition-models==0.3.0
numpy==1.19.3
opencv-python==4.4.0.46
Pillow==8.0.1
playsound==1.2.2
pytz==2020.4
sqlparse==0.4.1
```

---

## 🚀 Getting Started (5-Minute Setup)

> Tested on Windows with PowerShell. `dlib` requires CMake and a C++ compiler — see the note below if installation fails.

### 1. Clone the repository
```powershell
git clone https://github.com/Alokkumar12kk/face_recognition_attendance.git
```

### 2. Move into the project folder
The extracted/cloned folder may be nested (e.g. `face_recognition_attendance_system-dev`). You **must** `cd` into the folder containing `manage.py`, or you'll hit a *"no such file or directory"* error.
```powershell
cd face_recognition_attendance_system-dev
```

### 3. (Recommended) Create a virtual environment
```powershell
python -m venv venv
venv\Scripts\activate
```

### 4. Install dependencies
```powershell
pip install -r req.txt
```
> **If `dlib` fails to install:**
> - Install [CMake](https://cmake.org/download/) and add it to your PATH
> - Install *Visual Studio Build Tools* (Desktop development with C++ workload)
> - Re-run `pip install -r req.txt`

### 5. Run the development server
Open the project folder in VS Code, open a new terminal, and run:
```powershell
python manage.py runserver
```

### 6. Open the app
Visit **http://127.0.0.1:8000/** in your browser. 🎉

---

## 🔑 Admin Login

Default admin credentials (for local/dev use):

| Field    | Value   |
|----------|---------|
| Username | `arun`  |
| Password | `arun`  |

**To set your own credentials instead**, run:
```powershell
python manage.py createsuperuser
```
> ⚠️ Change the default credentials before deploying this anywhere beyond your local machine — they are intended for local testing only.

---

## 📁 Project Structure

```
face_recognition_attendance_system-dev/
├── attendance/              # Django app: models, views, dashboard logic
├── face_recognition_data/   # Face encodings / trained data
├── static/                  # CSS, JS, dashboard assets
├── templates/                # HTML templates (dashboard, tabs, etc.)
├── req.txt                  # Python dependencies
├── manage.py
└── README.md
```

---

## 🧭 Using the Dashboard

1. Log in with your admin credentials.
2. Go to **Employee Details** to register new profiles.
3. Click **Run Scanner** to start real-time face detection via webcam.
4. Recognized faces are logged automatically and appear under the **Present** tab.
5. Check the **Attendance** tab for full historical logs by Profile ID and timestamp.
6. Use **Reset** to clear the current session's present list, or **Refresh** to pull the latest data.

---

## 🗺️ Roadmap

- [ ] Multi-camera support
- [ ] Email/SMS alerts for absentees
- [ ] REST API for third-party integrations
- [ ] Mobile-friendly dashboard UI

---

## 🤝 Contributing

Contributions are welcome! Fork the repo, create a feature branch, and open a pull request.

```powershell
git checkout -b feature/your-feature-name
git commit -m "Add: your feature"
git push origin feature/your-feature-name
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

Built by **Alok Kumar** — Python Developer & AI Engineer.
Connect via [GitHub](https://github.com/Alokkumar12kk/) for questions, feedback, or collaboration.
