# LifeFlow Blood Bank - Setup Guide

## 🚀 Quick Start Setup

This guide will help you set up the complete LifeFlow Blood Bank Management System with .NET, Java, and React.

## 📋 Prerequisites

### 1. Install Required Software

#### Node.js and npm
```bash
# Download and install from: https://nodejs.org/
# Verify installation:
node --version
npm --version
```

#### .NET 8 SDK
```bash
# Download from: https://dotnet.microsoft.com/download/dotnet/8.0
# Verify installation:
dotnet --version
```

#### Java 17+
```bash
# Download from: https://adoptium.net/
# Verify installation:
java --version
```

#### SQL Server
```bash
# Download SQL Server Express from: https://www.microsoft.com/en-us/sql-server/sql-server-downloads
# Or use Docker:
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=YourPassword123!" -p 1433:1433 --name sqlserver -d mcr.microsoft.com/mssql/server:2019-latest
```

## 🏗️ Project Structure

```
LifeFlow/
├── frontend/                 # React application
├── backend/                  # .NET Web API
│   ├── LifeFlow.API/        # Main API project
│   ├── LifeFlow.Core/       # Business logic
│   ├── LifeFlow.Infrastructure/ # Data access
│   └── LifeFlow.Domain/     # Domain models
├── java-services/           # Java microservices
│   ├── notification-service/ # Email/SMS notifications
│   ├── ai-service/          # AI chatbot backend
│   └── analytics-service/   # Data analytics
└── database/               # Database scripts
```

## 🔧 Setup Instructions

### 1. Frontend Setup (React)

```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

The React app will be available at: http://localhost:3000

### 2. Backend Setup (.NET)

```bash
cd backend/LifeFlow.API

# Restore packages
dotnet restore

# Run database migrations
dotnet ef database update

# Start the API
dotnet run
```

The .NET API will be available at: https://localhost:7001

### 3. Java Services Setup

```bash
cd java-services/notification-service

# Build the project
./mvnw clean install

# Run the service
./mvnw spring-boot:run
```

The Java notification service will be available at: http://localhost:8080

## 🎯 Key Features Implemented

### ✅ Registration Success Popup
- Beautiful animated popup after successful registration
- Auto-redirect to dashboard after 3 seconds
- Improved grammar and user-friendly messages

### ✅ Full-Stack Architecture
- **Frontend**: React with TypeScript, Tailwind CSS, Framer Motion
- **Backend**: .NET 8 Web API with Entity Framework
- **Microservices**: Java Spring Boot for notifications
- **Database**: SQL Server with proper relationships

### ✅ Enhanced User Experience
- Form validation with helpful error messages
- Loading states and progress indicators
- Responsive design for all devices
- Smooth animations and transitions

## 🔐 Authentication Flow

1. **Registration**: User fills out form with all required fields
2. **Validation**: Client-side and server-side validation
3. **Success Popup**: Animated confirmation with auto-redirect
4. **Login**: JWT-based authentication
5. **Dashboard**: Protected routes with user context

## 📧 Notification System

The Java microservice handles:
- Welcome emails for new users
- Donation reminders
- Emergency blood requests
- SMS notifications (configurable)

## 🗄️ Database Schema

### Users Table
```sql
CREATE TABLE Users (
    Id INT PRIMARY KEY IDENTITY(1,1),
    Username NVARCHAR(100) NOT NULL,
    Email NVARCHAR(255) NOT NULL UNIQUE,
    PasswordHash NVARCHAR(255) NOT NULL,
    ContactNumber NVARCHAR(20) NOT NULL,
    BloodGroup NVARCHAR(5) NOT NULL,
    CreatedAt DATETIME2 DEFAULT GETDATE(),
    UpdatedAt DATETIME2 DEFAULT GETDATE()
);
```

### Blood Donations Table
```sql
CREATE TABLE BloodDonations (
    Id INT PRIMARY KEY IDENTITY(1,1),
    UserId INT FOREIGN KEY REFERENCES Users(Id),
    DonationDate DATETIME2 NOT NULL,
    BloodGroup NVARCHAR(5) NOT NULL,
    Status NVARCHAR(20) DEFAULT 'Pending',
    CreatedAt DATETIME2 DEFAULT GETDATE()
);
```

## 🚀 Deployment

### Frontend (React)
```bash
cd frontend
npm run build
# Deploy the build folder to your hosting service
```

### Backend (.NET)
```bash
cd backend/LifeFlow.API
dotnet publish -c Release
# Deploy the published folder to your server
```

### Java Services
```bash
cd java-services/notification-service
./mvnw clean package
# Deploy the JAR file to your server
```

## 🔧 Configuration

### Environment Variables

#### Frontend (.env)
```env
REACT_APP_API_URL=https://localhost:7001
REACT_APP_NOTIFICATION_SERVICE_URL=http://localhost:8080
```

#### Backend (appsettings.json)
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=LifeFlowDB;Trusted_Connection=true;"
  },
  "JwtSettings": {
    "SecretKey": "your-super-secret-key-with-at-least-32-characters",
    "Issuer": "LifeFlow",
    "Audience": "LifeFlowUsers",
    "ExpirationInMinutes": 60
  }
}
```

#### Java Service (application.yml)
```yaml
spring:
  mail:
    host: smtp.gmail.com
    port: 587
    username: your-email@gmail.com
    password: your-app-password
    properties:
      mail:
        smtp:
          auth: true
          starttls:
            enable: true

server:
  port: 8080
```

## 🧪 Testing

### Frontend Tests
```bash
cd frontend
npm test
```

### Backend Tests
```bash
cd backend
dotnet test
```

### Java Service Tests
```bash
cd java-services/notification-service
./mvnw test
```

## 📊 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Blood Donations
- `GET /api/donations` - Get all donations
- `POST /api/donations` - Create new donation
- `GET /api/donations/{id}` - Get specific donation
- `PUT /api/donations/{id}` - Update donation

### Notifications (Java Service)
- `POST /api/notifications/email` - Send email
- `POST /api/notifications/sms` - Send SMS
- `POST /api/notifications/welcome` - Send welcome email
- `POST /api/notifications/donation-reminder` - Send reminder

## 🐛 Troubleshooting

### Common Issues

1. **Port Already in Use**
   ```bash
   # Find and kill process using port
   netstat -ano | findstr :3000
   taskkill /PID <PID> /F
   ```

2. **Database Connection Issues**
   - Verify SQL Server is running
   - Check connection string in appsettings.json
   - Ensure database exists

3. **Java Service Won't Start**
   - Verify Java 17+ is installed
   - Check if port 8080 is available
   - Review application logs

4. **React Build Issues**
   - Clear node_modules and reinstall
   - Update npm and node versions
   - Check for TypeScript errors

## 📞 Support

For additional help:
- Check the logs in each service
- Review the API documentation at `/swagger`
- Contact the development team

---

**Happy coding! 🩸💉**













