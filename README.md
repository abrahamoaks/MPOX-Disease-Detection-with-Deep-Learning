# MPOX DETECTION API using COMPUTER VISION 

THIS REPOSITORY HOSTS THE CODE FOR A DEEP LEARNING-BASED MPOX DETECTION API, DESIGNED TO IDENTIFY MPOX LESIONS IN MEDICAL IMAGES USING A YOLO MODEL. THIS API IS INTENDED TO SUPPORT HEALTHCARE APPLICATIONS WHERE EFFICIENT AND ACCURATE DETECTION IS ESSENTIAL.

---

## 📜 PROJECT OVERVIEW

THE MPOX DETECTION API USES THE ULTRALYTICS YOLO MODEL TO ANALYZE MEDICAL IMAGES AND DETECT MPOX LESIONS. IF TWO OR MORE LESIONS ARE DETECTED IN AN IMAGE, THE API CLASSIFIES THE CASE AS "CONFIRMED." THIS PROJECT AIMS TO PROVIDE A TOOL FOR EARLY AND EFFICIENT MPOX DETECTION, PARTICULARLY FOR USE BY INNOVATEHEALTHAFRICA.

---

## 🚀 API USAGE

### ENDPOINT
- **URL**: `https://mpox-detection.onrender.com/detect`
- **METHOD**: `POST`

### PAYLOAD FORMAT
THE API EXPECTS IMAGES IN A MULTIPART FORM DATA UPLOAD. BELOW IS A SAMPLE PAYLOAD FOR REFERENCE:


{
  "files": [
    "image1.jpg"
  ]
}

### EXAMPLE REQUEST (USING CURL)

curl -X POST "https://mpox-detection.onrender.com/detect" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "files=@/path/to/your/image1.jpg"

### RESPONSE FORMAT

THE API RETURNS A JSON RESPONSE INDICATING THE STATUS OF THE CASE AND THE NUMBER OF DETECTIONS:

### EXAMPLE RESPONSE FOR CONFIRMED CASE:

{
  "status": "Confirmed Case",
  "detections": 3
}
### EXAMPLE RESPONSE FOR NOT CONFIRMED CASE:

{
  "status": "Not Confirmed",
  "detections": 0
}

## 🛠️ SETUP AND INSTALLATION

### REQUIREMENTS

	1.	PYTHON 3.8+
	2.	FASTAPI
	3.	ULTRALYTICS
	4.	PYTHON-MULTIPART (FOR HANDLING MULTIPART FORM DATA)

### INSTALLATION STEPS

	1.	CLONE THE REPOSITORY:

git clone https://github.com/abrahamoaks/MPOX_DISEASE_DETECTION.git
cd MPOX_DISEASE_DETECTION


	2.	INSTALL DEPENDENCIES:

pip install -r requirements.txt


	3.	START THE SERVER LOCALLY:

uvicorn main:app --host 0.0.0.0 --port 8000



## 📊 PROJECT DETAILS

	•	DATASET SOURCES: DATA WAS SOURCED FROM HEHEALTH AND AAGEE AI.
	•	DATA ANNOTATORS: ABRAHAM OBIANKE, YUSUF, AND ADESUNA.
	•	PROJECT MANAGEMENT AND MODEL DEVELOPMENT: ABRAHAM OBIANKE AND ISMAIL TIJJANI
	•	PROJECT PURPOSE: DEVELOPED PRIMARILY FOR INNOVATEHEALTHAFRICA TO ENHANCE EARLY DETECTION OF MPOX.

## ⚠️ LIMITATIONS AND FUTURE IMPROVEMENTS

	1.	DATA LIMITATIONS: DUE TO A LIMITED DATASET SIZE, THE MODEL MAY OVERFIT, LEADING TO POTENTIAL INACCURACIES IN NEW SCENARIOS.
	2.	LATENCY ISSUES: THE CURRENT HOST SIZE IS 502MB, RESULTING IN HIGHER LATENCY, ESPECIALLY IN REAL-TIME APPLICATIONS.
	3.	FUTURE IMPROVEMENTS: PLANS INCLUDE COLLECTING MORE DATA TO IMPROVE MODEL GENERALIZATION AND EXPLORING MODEL OPTIMIZATION TECHNIQUES TO REDUCE LATENCY.

## 📂 REPOSITORY STRUCTURE

	•	main.py: MAIN FASTAPI APPLICATION SCRIPT.
	•	requirements.txt: LIST OF REQUIRED PACKAGES.
	•	MODEL FILES: YOLO MODEL FILE (MPOX.pt).

## 💬 CONTACT

### 💬 Contact

For questions or feedback, please reach out to:

- **Email:** [abrahamoaks@gmail.com](mailto: abrahamoaks@gmail.com)
- **LinkedIn:**[(https://www.linkedin.com/in/abraham-obianke-269112197?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)](https://linkedin.com/in/abraham-obianke)

