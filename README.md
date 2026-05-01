Smart Gate Automation using License Plate Recognition
📖 Overview

This project implements an automated gate control system that identifies vehicles using license plate recognition. It leverages YOLOv8 for real-time plate detection and OCR for text extraction, then validates the result against a predefined whitelist. Authorized vehicles trigger automatic gate access.

🚀 Key Features
Real-time license plate detection using YOLOv8
Accurate text extraction with EasyOCR or Tesseract
Whitelist-based vehicle authorization
Automated gate operation via GPIO/relay interface
Modular architecture for scalability and customization
🛠️ Tech Stack
Python
YOLOv8 (Ultralytics)
OpenCV
EasyOCR / Tesseract
GPIO / Relay modules (hardware control)
📂 Project Structure
smart-gate-automation/
│── models/           # YOLOv8 model weights
│── src/
│   ├── main.py       # Application entry point
│   ├── detect.py     # License plate detection logic
│   ├── ocr.py        # OCR processing
│   ├── whitelist.py  # Authorization logic
│   └── gate.py       # Gate control interface
│── whitelist.json    # Authorized vehicle database
│── requirements.txt  # Dependencies
└── README.md
⚙️ Installation
git clone https://github.com/<your-username>/Smart-Gate-Automation-Using-License-Plate-Recognition.git
cd Smart-Gate-Automation-Using-License-Plate-Recognition
pip install -r requirements.txt

Download YOLOv8 weights:

yolo download yolov8n.pt
▶️ Usage
python src/main.py
System Workflow
Capture video frame
Detect license plate using YOLOv8
Extract text via OCR
Validate against whitelist
Trigger gate opening if authorized
📋 Whitelist Format
{
  "authorized_vehicles": [
    "BA1234",
    "GA5678",
    "LU9012"
  ]
}
🔒 Security Considerations
Protect and restrict access to the whitelist file
Use encryption for any remote/cloud communication
Maintain logs for monitoring and audit purposes
🌱 Future Enhancements
Cloud-based whitelist management
Mobile app for remote access control
Multi-camera support for larger deployments
Real-time alerts and monitoring dashboard
📜 License

This project is licensed under the MIT License.

👨‍💻 Author

Nischal Bhandari
GitHub: https://github.com/Nis6ha
