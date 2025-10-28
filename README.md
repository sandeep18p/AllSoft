# AllSoft Document Management System

A modern, responsive Document Management System built with React, featuring OTP-based authentication, file upload with tagging, search functionality, and document preview/download capabilities.

## Features

### 1. Authentication
- OTP-based login system using mobile number
- Secure token management
- Session persistence across page refreshes

### 2. File Upload
- Support for Image and PDF files only
- Date picker for document date selection
- Category selection (Personal/Professional)
- Dynamic dropdown for names (Personal) or departments (Professional)
- Tag management with autocomplete suggestions
- Remarks field for additional notes

### 3. File Search
- Search by category, dates, tags, and user
- Advanced filtering options
- Real-time search results

### 4. Document Management
- File preview for images and PDFs
- Individual file download
- Bulk download as ZIP (simulated)
- Document metadata display

### 5. Admin Panel
- User creation interface
- Admin management tools

## Technologies Used

- **React** 18.2.0 - UI Framework
- **React Router** 6.20.0 - Navigation and routing
- **Axios** 1.6.2 - HTTP client for API calls
- **Bootstrap** 5.3.2 - Responsive styling
- **React Bootstrap** 2.9.1 - Bootstrap components for React
- **React DatePicker** 4.24.0 - Date selection component
- **React Tag Input Component** 2.0.2 - Tag input functionality

## Project Structure

```
AllSoft/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── Login.js
│   │   ├── Dashboard.js
│   │   ├── UploadDocument.js
│   │   ├── SearchDocument.js
│   │   └── AdminPanel.js
│   ├── context/
│   │   └── AuthContext.js
│   ├── services/
│   │   └── api.js
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   └── index.css
├── package.json
└── README.md
```

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager
- Git for version control

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd AllSoft
```

2. Install dependencies:
```bash
npm install
```

## Running the Application

### Development Mode

Start the development server:
```bash
npm start
```

The application will open at `http://localhost:3000`

### Production Build

Create a production build:
```bash
npm run build
```

## Usage Guide

### 1. Login
- Enter your 10-digit mobile number
- Click "Send OTP"
- Enter the 6-digit OTP received
- Click "Verify OTP" to log in

### 2. Upload Document
- Navigate to "Upload Document" from the dashboard
- Select a file (Image or PDF only)
- Choose document date
- Select category (Personal/Professional)
- Select name or department from dropdown
- Add tags (with autocomplete suggestions)
- Enter remarks
- Click "Upload Document"

### 3. Search Documents
- Navigate to "Search Documents" from the dashboard
- Apply filters:
  - Select category
  - Enter name/department
  - Choose date range
  - Add tags
  - Enter user ID
- Click "Search"
- Preview or download documents from results

### 4. Admin Panel
- Navigate to "Admin Panel" from the dashboard
- Enter username and password
- Click "Create User"
- User creation is handled statically (backend integration required)

## API Integration

The application integrates with the following AllSoft APIs:

- **Base URL**: `https://apis.allsoft.co/api/documentManagement`

### Endpoints:
- `POST /generateOTP` - Generate OTP for mobile number
- `POST /validateOTP` - Validate OTP and get authentication token
- `POST /saveDocumentEntry` - Upload document with metadata
- `POST /searchDocumentEntry` - Search documents with filters
- `POST /documentTags` - Get available tags with suggestions

### Authentication
- Token is stored in localStorage after OTP validation
- Token is automatically included in API requests via axios interceptors

## Responsive Design

The application is fully responsive and optimized for:
- Desktop (1920px and above)
- Tablet (768px - 1024px)
- Mobile (320px - 767px)

## State Management

- Uses React Context API for authentication state
- Local component state for forms and UI
- Token persistence in localStorage

## Error Handling

- User-friendly error messages
- Loading states for async operations
- Validation for file types and form inputs

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Development Notes

- Bootstrap icons are used for visual elements (requires Bootstrap Icons CDN or package)
- All dates use ISO format for API communication
- File uploads support maximum file size as per backend configuration
- Tags are stored and retrieved from the backend

## Future Enhancements

- Bulk file upload
- Advanced search with filters
- File versioning
- Document sharing
- User roles and permissions
- Dashboard analytics
- Export search results

## Contributing

This is an assignment project for AllSoft. For any queries, contact: nk@allsoft.co

## License

This project is part of the AllSoft Document Management System assignment.

## Author

Developed as part of the AllSoft Front-End Developer assignment.

## Support

For any issues or queries regarding this implementation:
- Email: nk@allsoft.co
- Repository: [GitHub URL to be provided]

---

**Note**: This is a front-end implementation. The backend API is provided by AllSoft and should be running for full functionality.

