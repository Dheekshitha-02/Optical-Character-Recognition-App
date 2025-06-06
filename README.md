# Optical-Character-Recognition-Application
This project is a Flask-based web application that uses Tesseract OCR to extract text from uploaded images. It accepts images in .jpg, .jpeg, and .png formats, processes them into grayscale BMPs, and retrieves editable text using the Tesseract engine.

## 🚀 Key Features
- 🖼️ Upload images via web interface
- 🔤 Extracts printed text using Tesseract OCR
- 🧠 Auto-converts images to grayscale BMPs (Tesseract compatible)
- 📁 Saves output to text file and displays it in-browser
- 💡 Custom error handling for unsupported file types and OCR failures

## 🗂️ Project Structure
bash
```
ocr-app/
├── index.py              # Flask application routes
├── tasks.py              # Core logic for file handling and preprocessing
├── pytesser.py           # Tesseract integration and text extraction
├── util.py               # Helpers for image conversion and cleanup
├── errors.py             # Custom exceptions and log parsing
├── /images/
│   └── uploads/          # Directory to store uploaded images
├── /templates/
│   ├── index.html        # Home page
│   ├── form1.html        # Upload form
│   ├── display.html      # OCR output display
│   └── aboutus.html      # About page
├── output.txt            # Text file with OCR result
├── tesseract.log         # Log file for Tesseract errors
```

## ⚙️ Technologies Used
- Python 3
- Flask
- OpenCV / PIL (Pillow)
- Tesseract OCR
- HTML/CSS (Jinja2 templates)

## 💻 How to Run the Project
### 1. 📦 Install Required Packages
bash
```
pip install flask pillow
```
### 2. 🔧 Install Tesseract OCR
Windows: Tesseract Installer
Add Tesseract to your system PATH

### 3. 📂 Create Folder for Uploads
Ensure the folder images/uploads/ exists or create it manually:
bash
```
mkdir -p images/uploads
```
### 4. 🏁 Start the Flask App
bash
```
python index.py
```
### 5. 🌐 Open the link in the Browser

## 📌 Notes
- Only .png, .jpg, .jpeg files are allowed.
- Internally converts all images to 200 DPI grayscale BMP for better OCR accuracy.
- Tesseract log file is checked for errors and parsed using errors.py.



