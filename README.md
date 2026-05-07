# Cyber Security Student Complaint Management System

A full-stack web application for managing student complaints in a cyber security themed interface.
<img width="960" height="409" alt="Screenshot" src="https://github.com/user-attachments/assets/4d956ae5-c9a5-42ab-84bc-1c560d39237c" />

<img width="960" height="413" alt="Screenshot" src="https://github.com/user-attachments/assets/a6d3e8d5-652f-4854-93da-a28ef43fd5cc" />

<img width="949" height="413" alt="Screenshot" src="https://github.com/user-attachments/assets/f0c905a3-c6c1-4585-b0f9-c1422bab3de1" /> 
<img width="947" height="412" alt="Screenshot" src="https://github.com/user-attachments/assets/ce49ea9b-9c3c-424d-881f-e0e17f0ca76f" />
<img width="297" height="253" alt="Screenshot" src="https://github.com/user-attachments/assets/c4231fc6-a333-4edb-8a2e-e5a99140331f" /> 
<img width="947" height="414" alt="Screenshot" src="https://github.com/user-attachments/assets/0ea1101f-89c4-4c90-8d0d-15d41baecefd" />
<img width="946" height="413" alt="Screenshot" src="https://github.com/user-attachments/assets/f51eb942-f5fc-42b5-9562-1e50a344e576" /> 
<img width="946" height="413" alt="Screenshot" src="https://github.com/user-attachments/assets/ae2143a0-d4e1-4bf8-8416-006ea8d6fe97" />

## Features

- **User Roles**: Student, Staff, Admin
- **Complaint Management**: Create, track, and resolve complaints
- **Real-time Chat**: Socket.io powered messaging between students, staff and admin
- **File Uploads**: Support for attachments with complaints
- **Auto Assignment**: Automatic staff assignment based on complaint category
- **Admin Dashboard**: Comprehensive analytics and management tools
- **Responsive Design**: Mobile-first cyber security themed UI

***🔄 Core System Features**
Automated ticket ID generation (structured format)
Smart auto-routing based on complaint category
Role-based access control (Student, Staff, Admin)
Status lifecycle management system
Real-time communication and notifications
Secure file upload and storage
Activity logging for all actions
Response time tracking for each ticket

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- React Router
- Axios
- Socket.io Client

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT Authentication
- Multer (File Upload)
- Socket.io

## Project Structure

```
cyber-security-complaint-system/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── utils/
│   ├── uploads/
│   ├── server.js
│   ├── package.json
│   └── .env
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── package.json
│   └── tailwind.config.js
└── README.md
```

## Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- npm or yarn

### Backend Setup

1. Navigate to backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file in backend directory:
   ```env
   MONGO_URI=mongodb://localhost:27017/cyber-security-complaints
   JWT_SECRET=your_super_secret_jwt_key_here
   PORT=5000
   FRONTEND_URL=http://localhost:3000
   ```

4. Start MongoDB service (if using local MongoDB)

5. Start the backend server:
   ```bash
   npm run dev
   ```

### Frontend Setup

1. Navigate to frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

## Usage

1. **Register/Login**: Create an account or login with existing credentials
2. **Students**: Create complaints, view status, chat with staff
3. **Staff**: View assigned complaints, update status, respond to messages
4. **Admin**: Access admin panel for analytics and system management

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Complaints
- `POST /api/complaints` - Create complaint
- `GET /api/complaints` - Get user's complaints
- `GET /api/complaints/:id` - Get complaint by ID
- `PUT /api/complaints/:id/status` - Update complaint status
- `GET /api/complaints/admin/all` - Get all complaints (Admin)

### Messages
- `POST /api/messages` - Send message
- `GET /api/messages/:ticketId` - Get messages for ticket

## Ticket System

### Ticket ID Format
`HP-{CATEGORY}-{YEAR}-{NUMBER}`
Example: `HP-TECH-2026-0001`

### Auto Assignment Logic
- **Technical** → IT Staff
- **Accounts** → Finance Staff
- **Scholarship** → Scholarship Staff
- **Support** → Support Staff

### Status Flow
- New → OPEN
- Staff reply → IN_PROGRESS
- Need info → PENDING
- Student reply → IN_PROGRESS
- Staff resolves → RESOLVED
- Student accepts → CLOSED
- Student rejects → Reopen

## Security Features

- JWT-based authentication
- Password hashing with bcrypt
- Role-based access control
- Input validation and sanitization
- File upload restrictions

## Development

### Running Tests
```bash
# Backend tests (if implemented)
cd backend
npm test

# Frontend linting
cd frontend
npm run lint
```

### Building for Production
```bash
# Frontend build
cd frontend
npm run build

# Backend (no build needed for Node.js)
cd backend
npm start
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License.

## Support

For support, please contact the development team or create an issue in the repository.
