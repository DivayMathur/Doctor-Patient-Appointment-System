# Doctor-Patient Appointment System - CRUD Application

A complete Flask-based CRUD application for managing doctor-patient appointments with proper file structure and database integration.

## Features

### 👨‍⚕️ Doctor Management
- **Create**: Add new doctors with specialization and experience details
- **Read**: View all doctors or individual doctor profiles
- **Update**: Edit doctor information
- **Delete**: Remove doctors from the system
- View appointments associated with each doctor

### 🤒 Patient Management
- **Create**: Register new patients with medical history
- **Read**: View all patients or individual patient profiles
- **Update**: Edit patient information
- **Delete**: Remove patients from the system
- Track medical history and allergies

### 📅 Appointment Management
- **Create**: Schedule new appointments between doctors and patients
- **Read**: View all appointments with details
- **Update**: Modify appointment details, date, time, and status
- **Delete**: Cancel or remove appointments
- **Status Management**: Track appointment status (scheduled, completed, cancelled)
- **Notes**: Add notes to completed appointments

## Project Structure

```
appointment_system/
├── app/
│   ├── __init__.py              # Flask app factory
│   ├── models.py                # Database models (Doctor, Patient, Appointment)
│   ├── routes.py                # CRUD route handlers (blueprints)
│   ├── templates/
│   │   ├── base.html            # Base template with navigation
│   │   ├── index.html           # Dashboard
│   │   ├── doctors/
│   │   │   ├── list.html        # List all doctors
│   │   │   ├── create.html      # Create new doctor
│   │   │   ├── view.html        # View doctor details
│   │   │   └── edit.html        # Edit doctor information
│   │   ├── patients/
│   │   │   ├── list.html        # List all patients
│   │   │   ├── create.html      # Create new patient
│   │   │   ├── view.html        # View patient details
│   │   │   └── edit.html        # Edit patient information
│   │   └── appointments/
│   │       ├── list.html        # List all appointments
│   │       ├── create.html      # Schedule new appointment
│   │       ├── view.html        # View appointment details
│   │       └── edit.html        # Edit appointment
│   └── static/                  # Static files (CSS, JS, images)
├── instance/
│   └── appointment.db           # SQLite database (auto-created)
├── config.py                    # Configuration settings
├── run.py                       # Application entry point
├── requirements.txt             # Python dependencies
└── README.md                    # This file

```

## Database Models

### Doctor Model
- id (Primary Key)
- name (String)
- email (String, Unique)
- phone (String)
- specialization (String)
- experience_years (Integer)
- clinic_address (String)
- created_at (DateTime)

### Patient Model
- id (Primary Key)
- name (String)
- email (String, Unique)
- phone (String)
- date_of_birth (Date)
- gender (String)
- address (String)
- medical_history (Text)
- created_at (DateTime)

### Appointment Model
- id (Primary Key)
- doctor_id (Foreign Key)
- patient_id (Foreign Key)
- appointment_date (DateTime)
- reason_for_visit (String)
- status (String: scheduled, completed, cancelled)
- notes (Text)
- created_at (DateTime)

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Setup Instructions

1. **Clone or navigate to the project directory**
   ```bash
   cd appointment_system
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate

   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python run.py
   ```

5. **Access the application**
   - Open your browser and navigate to: `http://localhost:5000`
   - The database will be automatically created on first run

## Usage

### Dashboard
- Navigate to the home page to see statistics
- Quick access buttons to manage doctors, patients, and appointments

### Managing Doctors
1. Click "Doctors" in the navigation menu
2. Click "+ Add New Doctor" to create a new doctor
3. Fill in the required information and submit
4. View, edit, or delete doctors from the list

### Managing Patients
1. Click "Patients" in the navigation menu
2. Click "+ Add New Patient" to register a new patient
3. Enter patient details including medical history
4. View, edit, or delete patients from the list

### Managing Appointments
1. Click "Appointments" in the navigation menu
2. Click "+ New Appointment" to schedule an appointment
3. Select doctor and patient from dropdowns
4. Choose appointment date, time, and reason
5. View appointment details, mark as completed, or cancel

## API Routes

### Doctor Routes
- `GET /doctors/` - List all doctors
- `POST /doctors/create` - Create new doctor
- `GET /doctors/<id>` - View doctor details
- `POST /doctors/<id>/edit` - Update doctor
- `POST /doctors/<id>/delete` - Delete doctor

### Patient Routes
- `GET /patients/` - List all patients
- `POST /patients/create` - Create new patient
- `GET /patients/<id>` - View patient details
- `POST /patients/<id>/edit` - Update patient
- `POST /patients/<id>/delete` - Delete patient

### Appointment Routes
- `GET /appointments/` - List all appointments
- `POST /appointments/create` - Create new appointment
- `GET /appointments/<id>` - View appointment details
- `POST /appointments/<id>/edit` - Update appointment
- `POST /appointments/<id>/delete` - Delete appointment
- `POST /appointments/<id>/complete` - Mark as completed
- `POST /appointments/<id>/cancel` - Cancel appointment

## Technology Stack

- **Backend**: Flask 3.0.0
- **Database**: SQLite with SQLAlchemy ORM
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **Python**: 3.7+

## Features & CRUD Operations

### Create (C)
- Add new doctors with full details
- Register new patients with medical history
- Schedule appointments with date/time

### Read (R)
- View lists of all doctors, patients, appointments
- View detailed profiles with related information
- Dashboard with statistics

### Update (U)
- Edit doctor information and specialization
- Update patient details and medical history
- Modify appointment details, dates, and status

### Delete (D)
- Remove doctors from the system (cascade deletes appointments)
- Delete patient records (cascade deletes appointments)
- Cancel or remove appointments

## Configuration

Edit `config.py` to modify:
- Database location and type
- Debug mode
- Secret key for production

## Future Enhancements

- User authentication and authorization
- Appointment notifications/reminders
- Doctor availability scheduling
- Patient feedback and ratings
- Search and filter functionality
- Appointment history archives
- PDF report generation
- Email notifications

## Troubleshooting

### Database Issues
- Delete `instance/appointment.db` to reset the database
- The database will be recreated on next run

### Port Already in Use
- Change the port in `run.py` from 5000 to another available port
- Or kill the process using the port

### Template Not Found
- Ensure all template files are in the correct directories
- Check file names match exactly (case-sensitive on Linux/Mac)

## License

This project is open source and available under the MIT License.

## Author

Created as a comprehensive Flask CRUD application for managing medical appointments.

## Support

For issues or questions, check the application logs for detailed error messages.
