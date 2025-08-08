# LifeFlow - Blood Bank Management System

A comprehensive full-stack blood bank management system built with modern technologies.

## 🏗️ Architecture

### Frontend
- **React 18** with TypeScript
- **Tailwind CSS** for styling
- **Framer Motion** for animations
- **React Hook Form** for form management
- **React Hot Toast** for notifications

### Backend APIs
- **.NET 8 Web API** - Main application API
- **Java Spring Boot** - Microservices for specialized features
- **Entity Framework Core** - ORM for .NET
- **SQL Server** - Primary database

### Features
- ✅ User authentication and authorization
- ✅ Blood donation management
- ✅ Blood bank locator
- ✅ AI-powered chatbot
- ✅ Real-time notifications
- ✅ 3D animations and modern UI
- ✅ Multi-step donation forms
- ✅ Blood inventory management
- ✅ Emergency blood requests
- ✅ Donor health tracking

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- .NET 8 SDK
- Java 17+
- SQL Server 2019+

### Frontend (React)
```bash
cd frontend
npm install
npm start
```

### Backend (.NET API)
```bash
cd backend/LifeFlow.API
dotnet restore
dotnet run
```

### Java Microservices
```bash
cd java-services
./mvnw spring-boot:run
```

## 📁 Project Structure

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

## 🔧 Configuration

### Database Connection
Update connection strings in `appsettings.json`:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=LifeFlowDB;Trusted_Connection=true;"
  }
}
```

### API Endpoints
- **.NET API**: `https://localhost:7001`
- **Java Services**: `https://localhost:8080`
- **React App**: `http://localhost:3000`

## 🎯 Key Features

### 1. User Management
- Registration with blood group
- Login/logout functionality
- Profile management
- Role-based access control

### 2. Blood Donation
- Multi-step donation form
- Eligibility checking
- Appointment scheduling
- Donation history tracking

### 3. Blood Bank Locator
- Find nearby blood banks
- Real-time availability
- Distance calculation
- Contact information

### 4. AI Assistant
- Intelligent chatbot
- Blood donation guidance
- FAQ automation
- Health recommendations

### 5. Emergency System
- Emergency blood requests
- Real-time notifications
- Donor matching
- Priority handling

## 🛠️ Development

### Adding New Features
1. Create domain models in `LifeFlow.Domain`
2. Add business logic in `LifeFlow.Core`
3. Implement API endpoints in `LifeFlow.API`
4. Update React components in `frontend`
5. Add tests in respective test projects

### Database Migrations
```bash
cd backend/LifeFlow.API
dotnet ef migrations add MigrationName
dotnet ef database update
```

## 📊 API Documentation

### Authentication
```
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
```

### Blood Donation
```
GET /api/donations
POST /api/donations
GET /api/donations/{id}
PUT /api/donations/{id}
```

### Blood Banks
```
GET /api/bloodbanks
GET /api/bloodbanks/nearby
GET /api/bloodbanks/{id}
```

### Users
```
GET /api/users/profile
PUT /api/users/profile
GET /api/users/donations
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
cd java-services
./mvnw test
```

## 🚀 Deployment

### Production Build
```bash
# Frontend
cd frontend
npm run build

# Backend
cd backend/LifeFlow.API
dotnet publish -c Release

# Java Services
cd java-services
./mvnw clean package
```

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## 📞 Support

For support and questions:
- Email: support@lifeflow.com
- Documentation: file:///C:/Users/adity/Desktop/Blood%20bank/blood-bank-india-3d.html
- Issues: GitHub Issues

---

**Built with ❤️ for saving lives through blood donation**
