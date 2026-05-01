# Smart Gate Automation using License Plate Recognition

## 📖 Overview
A smart gate automation system that uses **YOLOv8** to detect license plates, applies **OCR** to extract text, and checks against a **whitelist**. If the vehicle is authorized, the gate opens automatically.

---

## 🚀 Features
- Real‑time license plate detection with YOLOv8
- OCR text extraction (EasyOCR/Tesseract)
- Whitelist verification for authorized vehicles
- Automated gate control via GPIO/relay
- Modular design for easy extension

---

## 🛠️ Tech Stack
- Python
- YOLOv8 (Ultralytics)
- OpenCV
- EasyOCR / Tesseract
- GPIO/Relay (for hardware control)

---

## 📂 Structure
smart-gate-automation/
│── models/           # YOLOv8 weights
│── src/
│   ├── main.py       # Entry point
│   ├── detect.py     # License plate detection
│   ├── ocr.py        # OCR extraction
│   ├── whitelist.py  # Whitelist logic
│   └── gate.py       # Gate control
│── whitelist.json    # Authorized vehicles
│── requirements.txt  # Dependencies
└── README.md

Code

---

## ⚙️ Installation
```bash
git clone https://github.com/<your-username>/Smart-Gate-Automation-Using-License-Plate-Recognition.git
cd Smart-Gate-Automation-Using-License-Plate-Recognition
pip install -r requirements.txt
Download YOLOv8 weights:

bash
yolo download yolov8n.pt
▶️ Usage
bash
python src/main.py
Flow:

Capture video frame

Detect license plate (YOLOv8)

Extract text (OCR)

Check whitelist

Open gate if authorized

📋 Whitelist Example
json
{
  "authorized_vehicles": [
    "BA1234",
    "GA5678",
    "LU9012"
  ]
}
🔒 Security
Keep whitelist secure

Use encrypted communication if cloud‑connected

Add logging for audit trails

🌟 Future Work
Cloud whitelist management

Mobile app integration

Multi‑camera support

Real‑time notifications

📜 License
MIT License

👨‍💻 Author
Nischal Bhandari  
GitHub: Nis6hal
