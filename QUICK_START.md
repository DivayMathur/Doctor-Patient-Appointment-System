# Quick Start Guide

## 1. Installation & Setup

### Windows
```bash
# Navigate to project directory
cd appointment_system

# Create virtual environment
python -m venv venv

# Activate virtual environment
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the application
python run.py
```

### macOS/Linux
```bash
# Navigate to project directory
cd appointment_system

# Create virtual environment
python3 -m venv venv

# Activate virtual environment
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the application
python run.py
```

## 2. Access the Application

Open your browser and go to: **http://localhost:5000**

## 3. Create Sample Data

1. **Add Doctors**
   - Navigate to "Doctors" → "Add New Doctor"
   - Fill in the doctor details
   - Click "Create Doctor"

2. **Add Patients**
   - Navigate to "Patients" → "Add New Patient"
   - Fill in the patient details including medical history
   - Click "Create Patient"

3. **Schedule Appointments**
   - Navigate to "Appointments" → "New Appointment"
   - Select a doctor and patient
   - Choose date and time
   - Enter reason for visit
   - Click "Create Appointment"

## 4. Navigation Features

### Dashboard
- Overview of total doctors, patients, and appointments
- Quick access to create new records

### Doctors
- View all doctors with specialization
- Click on a doctor to see full profile and appointments
- Edit or delete doctor records

### Patients
- View all patients with contact information
- Click on a patient to see medical history and appointments
- Edit or delete patient records

### Appointments
- View all scheduled appointments
- Filter by status (scheduled, completed, cancelled)
- Mark appointments as completed with notes
- Cancel appointments if needed

## 5. Database

- SQLite database automatically created at: `instance/appointment.db`
- To reset database: Delete `instance/appointment.db` and restart the app

## 6. Common Operations

### Creating a Doctor
```
Name: Dr. John Smith
Email: john.smith@clinic.com
Phone: +1-555-123-4567
Specialization: Cardiology
Experience: 10 years
Address: 123 Medical Complex, City
```

### Creating a Patient
```
Name: Jane Doe
Email: jane.doe@email.com
Phone: +1-555-987-6543
DOB: 1990-05-15
Gender: Female
Address: 456 Main Street, City
Medical History: Hypertension, Allergic to Penicillin
```

### Scheduling an Appointment
```
Doctor: Dr. John Smith (Cardiology)
Patient: Jane Doe
Date: 2024-03-15
Time: 14:30
Reason: Regular checkup and blood pressure consultation
Status: Scheduled
```

## 7. Troubleshooting

**Port 5000 already in use?**
- Edit `run.py` and change port number in the last line

**Database errors?**
- Delete `instance/appointment.db`
- Restart the application

**Template not found error?**
- Ensure you're running from the project root directory
- Check that `templates/` folder exists with all HTML files

## Features Overview

✅ **Complete CRUD Operations**
- Create doctors, patients, and appointments
- Read/View all records
- Update existing information
- Delete records

✅ **Professional UI**
- Bootstrap 5 responsive design
- Intuitive navigation
- Status badges for appointments
- Confirmation dialogs for deletions

✅ **Data Relationships**
- Doctors connected to appointments
- Patients connected to appointments
- Cascade delete for data integrity

✅ **Appointment Management**
- Schedule appointments with date and time
- Track appointment status
- Add notes to completed appointments
- Cancel appointments

## Next Steps

1. Explore the application
2. Add sample doctors and patients
3. Schedule appointments
4. Test all CRUD operations
5. Check the README.md for more details

Enjoy using the Doctor-Patient Appointment System!
