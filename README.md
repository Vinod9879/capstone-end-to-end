# Document Verification System

A comprehensive document verification system with React frontend, ASP.NET Core backend, and DLL integration for EC, Aadhaar, and PAN document processing.

## 🎯 Features

### User Dashboard
- Document upload (EC, Aadhaar, PAN)
- Real-time verification status
- Risk score calculation
- Upload history tracking
- Extracted data display

### Admin Dashboard
- User management
- Document monitoring
- Analytics and reports
- Activity logs
- Verification oversight

### Document Processing
- PDF extraction using DLL
- Field-by-field comparison
- Risk score calculation
- Verification notes
- Mismatch detection

## 🛠️ Technology Stack

### Frontend
- **React 18.2.0** - UI framework
- **Bootstrap 5.3.0** - Styling
- **Axios 1.4.0** - HTTP client
- **React Router 6.11.0** - Navigation

### Backend
- **ASP.NET Core 8.0** - Web API
- **Entity Framework Core** - Database ORM
- **SQL Server** - Database
- **JWT Authentication** - Security

### Document Processing
- **Custom DLL** - PDF extraction
- **Risk Calculation** - Scoring algorithm
- **File Management** - Document storage

## 📁 Project Structure

```
DocumentVerificationSystem/
├── webApitest/                 # ASP.NET Core Backend
│   ├── Controllers/            # API Controllers
│   ├── Models/                 # Data Models
│   ├── Services/               # Business Logic
│   ├── Data/                   # Database Context
│   └── DTOs/                   # Data Transfer Objects
├── react-contacts-app/         # React Frontend
│   ├── src/
│   │   ├── Components/        # React Components
│   │   ├── Services/           # API Services
│   │   └── Routes/             # Navigation
│   └── public/                 # Static Files
└── DocumentVerificationDLL/    # Document Processing DLL
    └── DocumentVerificationDLL/
        ├── IDocumentVerificationDLL.cs
        └── DocumentVerificationDLL.cs
```

## 🚀 Getting Started

### Prerequisites
- .NET 8.0 SDK
- Node.js 18+
- SQL Server
- Visual Studio Code or Visual Studio

### Backend Setup
```bash
cd webApitest
dotnet restore
dotnet run
```

### Frontend Setup
```bash
cd react-contacts-app
npm install
npm start
```

### Database Setup
1. Update connection string in `appsettings.json`
2. Run Entity Framework migrations
3. Seed initial data

## 📊 API Endpoints

### User Dashboard APIs
- `GET /api/UserDashboard/profile` - Get user profile
- `PUT /api/UserDashboard/profile` - Update profile
- `POST /api/UserDashboard/upload-documents` - Upload documents
- `GET /api/UserDashboard/document-status` - Get status
- `POST /api/UserDashboard/verify-documents` - Verify documents

### Admin Dashboard APIs
- `GET /api/AdminDashboard/users` - Get all users
- `GET /api/AdminDashboard/documents` - Get all documents
- `GET /api/AdminDashboard/analytics` - Get analytics
- `POST /api/AdminDashboard/documents/{id}/verify` - Trigger verification

## 🔧 Configuration

### Backend Configuration
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=DocumentVerification;Trusted_Connection=true;"
  },
  "JwtSettings": {
    "SecretKey": "your-secret-key",
    "Issuer": "DocumentVerification",
    "Audience": "DocumentVerification"
  }
}
```

### Frontend Configuration
```javascript
const API_BASE_URL = 'https://localhost:5194/api';
```

## 📱 Screenshots

### User Dashboard
- Document upload interface
- Verification status display
- Upload history table
- Risk score visualization

### Admin Dashboard
- User management interface
- Document monitoring
- Analytics dashboard
- Activity logs

## 🔒 Security Features

- JWT Authentication
- Role-based authorization
- File upload validation
- CORS configuration
- Input sanitization

## 📈 Performance

- Async/await patterns
- Database optimization
- File caching
- Response compression

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👥 Authors

- Your Name - Initial work

## 🙏 Acknowledgments

- Document processing libraries
- React community
- ASP.NET Core team