# Installation and Setup Instructions

## For Windows Users

### Option 1: Using Batch File (Easiest)
1. Double-click `run.bat` in the appointment_system folder
2. The application will start on http://localhost:5000

### Option 2: Manual Setup with Command Prompt
```cmd
cd c:\Users\ASUS\OneDrive\文档\My oproje\appointment_system
python run.py
```

Then open http://localhost:5000 in your browser.

## For Mac/Linux Users

```bash
cd ~/OneDrive/文档/My\ oproje/appointment_system
python3 run.py
```

Then open http://localhost:5000 in your browser.

## Troubleshooting

If you get `ModuleNotFoundError: No module named 'flask_sqlalchemy'`:

```bash
cd appointment_system
pip install -r requirements.txt
python run.py
```

## First Run

- The database will be automatically created at `instance/appointment.db`
- Navigate to http://localhost:5000
- Start adding doctors, patients, and appointments!

## Stop the Application

Press `Ctrl+C` in the terminal to stop the Flask server.
