# Smart Clinic Database Schema

## Tables

### Doctor
- id (INT, PK, AUTO_INCREMENT)
- name (VARCHAR(100))
- email (VARCHAR(100), UNIQUE)
- specialty (VARCHAR(50))
- availableTimes (JSON)

### Patient
- id (INT, PK, AUTO_INCREMENT)
- name (VARCHAR(100))
- email (VARCHAR(100), UNIQUE)
- phone (VARCHAR(15))
- dob (DATE)

### Appointment
- id (INT, PK, AUTO_INCREMENT)
- doctor_id (INT, FK → Doctor.id)
- patient_id (INT, FK → Patient.id)
- appointment_time (DATETIME)
- status (VARCHAR(20))

### Prescription
- id (INT, PK, AUTO_INCREMENT)
- appointment_id (INT, FK → Appointment.id)
- doctor_id (INT, FK → Doctor.id)
- patient_id (INT, FK → Patient.id)
- prescription_text (TEXT)
