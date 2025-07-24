# Hospital Management System

A simple console-based Hospital Management System built with Java and MySQL for managing patients, doctors, and appointments.

## Features

- **Patient Management**: Add new patients and view patient records
- **Doctor Management**: View available doctors and their specializations
- **Appointment Booking**: Schedule appointments between patients and doctors
- **Doctor Availability**: Check if doctors are available on specific dates

## Tech Stack

- **Language**: Java
- **Database**: MySQL
- **JDBC Driver**: MySQL Connector/J 8.3.0

## Database Schema

The system uses three main tables:
- `patients` - stores patient information (id, name, age, gender)
- `doctors` - stores doctor details (id, name, specialization)
- `appointments` - manages appointments (patient_id, doctor_id, appointment_date)

## How to Run

1. **Prerequisites**:
   - Java Development Kit (JDK)
   - MySQL Server
   - MySQL Connector/J driver

2. **Database Setup**:
   - Create a MySQL database named `Hospital`
   - Update connection details in `HospitalManagementSystem.java`:
     ```java
     private static final String url = "jdbc:mysql://localhost:3306/Hospital";
     private static final String username = "your_username";
     private static final String password = "your_password";
     ```

3. **Run the Application**:
   ```bash
   javac -cp ".:mysql-connector-j-8.3.0.jar" HospitalManagementSystem/*.java
   java -cp ".:mysql-connector-j-8.3.0.jar" HospitalManagementSystem.HospitalManagementSystem
   ```

## Usage

The system provides a menu-driven interface:
1. Add Patient - Register new patients
2. View Patients - Display all registered patients
3. View Doctors - Show available doctors
4. Book Appointment - Schedule patient-doctor appointments
5. Exit - Close the application

## Project Structure

```
Hospital Management System/
├── src/
│   ├── HospitalManagementSystem/
│   │   ├── HospitalManagementSystem.java  # Main class
│   │   ├── Patient.java                   # Patient operations
│   │   └── Doctors.java                   # Doctor operations
│   └── Main.java
└── Hospital Management System.iml
```

## Key Learning Points

- JDBC connectivity with MySQL
- PreparedStatement usage for SQL injection prevention
- Object-oriented design with separate classes for different entities
- Basic exception handling
- Console-based user interface design

## Future Enhancements

- Add GUI using JavaFX or Swing
- Implement user authentication
- Add more detailed patient medical records
- Include billing and payment management
- Add appointment time slots instead of just dates
