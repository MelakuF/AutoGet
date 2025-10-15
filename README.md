# Care Management System

A comprehensive care management system for managing drivers across multiple stations with QR code-based attendance tracking.

## Features

### Admin Dashboard

- Register and manage sub-admins (station managers)
- View system-wide statistics
- Control sub-admin access and activity
- Monitor all stations from one central location

### Sub-Admin Dashboard

- Manage drivers at your station
- Add, edit, and delete driver information
- View station-specific statistics
- Access QR code scanning
- Generate daily reports

### Driver Management

- Register drivers with complete information:
  - Driver name
  - Driver license number
  - Car model
  - Car plate number
- Automatic QR code generation (check-in and check-out)
- Print driver profiles with QR codes
- Edit and delete driver records

### QR Code System

- Automatic generation of 2 QR codes per driver:
  - Green QR code for check-in
  - Red QR code for check-out
- Real-time QR code scanning with camera
- Instant attendance logging
- Driver information display on scan

### Reporting

- Daily attendance reports
- Check-in/check-out tracking
- Export reports to CSV
- Print-friendly report format
- Real-time statistics

### Security

- Role-based access control (Admin and Sub-Admin)
- Isolated data per station
- Secure authentication with JWT
- Password hashing with bcrypt
- Session management

## Getting Started

### Prerequisites

- Supabase account (database integration)
- Modern web browser with camera access

### Installation

1. Run the SQL scripts in order:
   - `scripts/01-create-tables.sql` - Creates database tables
   - `scripts/02-seed-admin.sql` - Creates default admin account

2. Default admin credentials:
   - Email: <admin@caremanagement.com>
   - Password: Admin@123

### Usage

#### As Admin

1. Login with admin credentials
2. Create sub-admins for each station
3. Monitor system-wide activity
4. Manage sub-admin access

#### As Sub-Admin

1. Login with your credentials
2. Add drivers to your station
3. Print driver profiles with QR codes
4. Scan QR codes for attendance
5. View daily reports

#### Driver Attendance

1. Print driver profile with QR codes
2. Driver scans green QR code on arrival
3. Driver scans red QR code on departure
4. View attendance in daily reports

## Technology Stack

- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **Backend**: Next.js API Routes, Server Actions
- **Database**: Supabase (PostgreSQL)
- **Authentication**: JWT with bcrypt
- **QR Codes**: qrcode library for generation, html5-qrcode for scanning

## Database Structure

- `admins` - Main administrators
- `sub_admins` - Station managers
- `drivers` - Driver information and QR codes
- `attendance_logs` - Check-in/check-out records

## Key Features

- **Isolated Data**: Each sub-admin only sees their own drivers
- **Automatic QR Generation**: QR codes created on driver registration
- **Real-time Scanning**: Instant attendance logging with camera
- **Comprehensive Reports**: Daily reports with export functionality
- **Print-Ready Profiles**: Professional driver profiles with QR codes
- **Responsive Design**: Works on desktop and mobile devices

## Support

For issues or questions, contact your system administrator.
