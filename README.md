# Smart Gate Automation using License Plate Recognition

## 📖 Overview
This project implements a smart gate system that detects vehicle license plates using **YOLOv8**, extracts text via **OCR**, and processes access decisions. It supports **ESP32-based gate control**, a **web dashboard**, and optional **Blynk integration**.

---

## 🚀 Features
- Real-time license plate detection (YOLOv8)
- OCR-based plate text extraction
- Gate control via ESP32
- Web dashboard for monitoring and control
- Logging using CSV and SQLite
- Optional IoT integration with Blynk
- Multiple execution modes

---

## 🛠️ Tech Stack
- Python  
- YOLOv8 (Ultralytics)  
- OpenCV  
- EasyOCR / Tesseract  
- Flask  
- ESP32  
- Blynk  
- SQLite + CSV  

---

## 📂 Project Structure
```text
.
├── templates/
│   ├── admin.html         # Admin panel UI
│   ├── dashboard.html     # Dashboard interface
│   ├── layout.html        # Shared layout
│   └── login.html         # Login page
├── .gitattributes
├── IPforESP32.txt         # ESP32 IP address
├── README.md
├── access_log.db          # SQLite logs
├── app.py                 # Flask backend
├── main.py                # Main script (with video)
├── main-novideofeed.py    # Run without video
├── testwithblynk.py       # Blynk testing
├── best.pt                # YOLOv8 model
├── plate_log.csv          # Detection logs
├── requirements.txt
```

---

## ⚙️ Installation
```bash
git clone https://github.com/<your-username>/Smart-Gate-Automation-Using-License-Plate-Recognition.git
cd Smart-Gate-Automation-Using-License-Plate-Recognition
pip install -r requirements.txt
```

Make sure `best.pt` is available.

---

## ▶️ Usage

### Run detection system
```bash
python main.py
```

### Run without video feed
```bash
python main-novideofeed.py
```

### Run web dashboard
```bash
python app.py
```

### Test Blynk
```bash
python testwithblynk.py
```

---

## 🌐 Web Interface
- `/login` → Login page  
- `/dashboard` → Monitoring interface  
- `/admin` → Admin controls  

---

## 🔄 Workflow
1. Capture frame  
2. Detect plate (YOLOv8)  
3. Extract text (OCR)  
4. Log result  
5. Trigger ESP32 if authorized  
6. Update dashboard / Blynk  

---

## 📡 ESP32 Setup
- Store IP in `IPforESP32.txt`  
- Ensure same network  
- Configure relay for gate  

---

## 📊 Logging
- `plate_log.csv` → raw detections  
- `access_log.db` → structured logs  

---

## 🔒 Security
- Protect dashboard routes  
- Restrict ESP32 access  
- Validate requests  
- Monitor logs  

---

## 🌱 Future Work
- Whitelist system  
- API integration  
- Cloud deployment  
- Notifications  

---

## 📜 License
MIT License  

---

## 👨‍💻 Author
**Aaditya Baral**
https://github.com/aadityabaral17

**Ayush Khanal** 
https://github.com/khanalayush

**Nischal Bhandari**  
https://github.com/Nis6hal

**Samyog Sapkota**

