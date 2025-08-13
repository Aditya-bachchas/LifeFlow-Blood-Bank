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

git checkout -b add-website-preview

## 🌐 Website Preview  

**Preview:** After executing this code, it will look like this:
 "[LifeFlow Blood bank](https://16331842-02a9-4e87-9a93-490cc2278218-00-fbwrvpapqpkf.riker.replit.dev/)"
 
 <img width="959" height="449" alt="image" src="https://github.com/user-attachments/assets/c7903ffe-7c19-456b-848d-cd4b24ed3ae0" />
 <img width="959" height="449" alt="image" src="https://github.com/user-attachments/assets/e8c98550-ffcf-4c43-ae1f-93fe8d154761" />
 <img width="959" height="444" alt="image" src="https://github.com/user-attachments/assets/789bc5ca-5afe-416a-aed6-38415206347c" />
 <img width="946" height="436" alt="image" src="https://github.com/user-attachments/assets/46a50c7e-7a5b-402e-b04e-ea0bc9b577b3" />
 <img width="959" height="449" alt="image" src="https://github.com/user-attachments/assets/bd5087f2-a261-47ea-bf07-2e3b6f206f5d" />
 <img width="958" height="442" alt="image" src="https://github.com/user-attachments/assets/60f1b7c8-f4c6-461b-b8ae-a33eddd63e3e" />
 <img width="959" height="439" alt="image" src="https://github.com/user-attachments/assets/7b11bdd4-babf-4b9e-b406-f9d172afdd9e" />
 <img width="959" height="443" alt="image" src="https://github.com/user-attachments/assets/563c85fb-ee14-4c25-a5d2-5f07f2d4b76e" />
 <img width="959" height="440" alt="image" src="https://github.com/user-attachments/assets/8bc140c8-1633-47b9-9421-09c1760827dd" />
 <img width="957" height="436" alt="image" src="https://github.com/user-attachments/assets/f394f9aa-39fe-4fc4-ab15-100162519330" />

**Rechange:** This code has been slightly customized for an Indian website.   "[LifeFlow Blood bank](https://3fbb1138-223a-4fe5-83ff-51f589abea1a-00-2jk7uub6jg4ts.spock.replit.dev/)"

 <img width="947" height="413" alt="image" src="https://github.com/user-attachments/assets/722bd0c8-90ef-4663-a3a0-18319b2605e6" />
 <img width="959" height="411" alt="image" src="https://github.com/user-attachments/assets/19435186-fc16-44fd-bcd4-d9e1b8c17b0a" />
 <img width="959" height="406" alt="image" src="https://github.com/user-attachments/assets/d71b3f1d-6ae0-4e00-85ec-ebe59f19a321" />
 <img width="959" height="409" alt="image" src="https://github.com/user-attachments/assets/aaa8271b-a1ee-4c13-8489-7aa18b72b2d8" />
 <img width="959" height="356" alt="image" src="https://github.com/user-attachments/assets/49baaf80-78cd-4d75-af8c-3066ec999819" />
 <img width="947" height="355" alt="image" src="https://github.com/user-attachments/assets/702908c1-18f0-4bb0-9ab4-ccc527debf7e" />

 

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
- Documentation: [Download](https://drive.google.com/drive/folders/1CXPz8EGMLmD5cCMiGvWYP6J2O8aE6e4H)
- Issues: GitHub Issues

---

**Built with ❤️ for saving lives through blood donation**
