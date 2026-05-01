# Smart Gate Automation using License Plate Recognition

## 📖 Overview
This project implements an automated gate control system that identifies vehicles using license plate recognition. It uses **YOLOv8** for detection and **OCR** for text extraction, then verifies the result against a whitelist. Authorized vehicles trigger automatic gate access.

---

## 🚀 Key Features
- Real-time license plate detection using YOLOv8  
- Text extraction with EasyOCR or Tesseract  
- Whitelist-based authorization  
- Automated gate control via GPIO/relay  
- Modular and extensible design  

---

## 🛠️ Tech Stack
- Python  
- YOLOv8 (Ultralytics)  
- OpenCV  
- EasyOCR / Tesseract  
- GPIO / Relay modules  

---

## 📂 Project Structure
```text
smart-gate-automation/
│── models/           # YOLOv8 model weights
│── src/
│   ├── main.py       # Entry point
│   ├── detect.py     # Plate detection
│   ├── ocr.py        # OCR processing
│   ├── whitelist.py  # Authorization logic
│   └── gate.py       # Gate control
│── whitelist.json    # Authorized vehicles
│── requirements.txt
└── README.md
```

---

## ⚙️ Installation
```bash
git clone https://github.com/<your-username>/Smart-Gate-Automation-Using-License-Plate-Recognition.git
cd Smart-Gate-Automation-Using-License-Plate-Recognition
pip install -r requirements.txt
```

Download YOLOv8 weights:
```bash
yolo download yolov8n.pt
```

---

## ▶️ Usage
```bash
python src/main.py
```

### Workflow
1. Capture video frame  
2. Detect license plate  
3. Extract text (OCR)  
4. Check whitelist  
5. Open gate if authorized  

---

## 📋 Whitelist Example
```json
{
  "authorized_vehicles": [
    "BA1234",
    "GA5678",
    "LU9012"
  ]
}
```

---

## 🔒 Security
- Keep whitelist protected  
- Use encryption for remote systems  
- Enable logging for audits  

---

## 🌱 Future Work
- Cloud-based whitelist  
- Mobile app integration  
- Multi-camera support  
- Real-time alerts  
