# cv_agent


This project provides a FastAPI-based web service that converts PDF resumes to JSON, then to LaTeX format, and finally generates a new PDF.

🌟 Features
📤 Upload PDF files
🔄 Convert PDF to JSON
✏️ Edit JSON data
📝 Generate LaTeX from JSON
📄 Compile LaTeX to PDF
Prerequisites
Python 3.7+
FastAPI
pdflatex
Installing pdflatex
macOS:
Install MacTeX (full TeX Live distribution):

brew install --cask mactex
Or for a smaller installation, use BasicTeX:

brew install --cask basictex
After installation, make sure to add the LaTeX binaries to your PATH:

export PATH="/Library/TeX/texbin:$PATH"
Linux (Ubuntu/Debian):
Install TeX Live:
sudo apt-get update
sudo apt-get install texlive-full
For a minimal installation:
sudo apt-get install texlive-latex-base
🛠️ Installation
Clone the repository:

git clone https://github.com/iptv-cloud/cv_agent
cd resume_agent
Install dependencies:

pip install fastapi uvicorn python-multipart
Ensure pdflatex is installed on your system.

Usage
Start the server:

python main.py
Access the web interface at http://localhost:8000

Upload a PDF file, edit the JSON data if needed, and generate the new PDF.

🔗 API Endpoints
POST /upload: Upload a PDF file
POST /generate: Generate PDF from JSON data
GET /: Serve the main HTML page
📁 Project Structure
input/: Directory for input files
output/: Directory for output files
src/: Source code directory
pdf2json.py: PDF to JSON conversion
json2tex.py: JSON to LaTeX conversion
header_eng.tex: LaTeX header template
static/: Static files for the web interface
main.py: Main FastAPI application
