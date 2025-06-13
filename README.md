# ShiftEase+

An intelligent shift and time-off management system with role-based dashboards built using React and Express.js.

## Features

- **Role-based Access Control**: Admin, Manager, and Employee roles with specific permissions
- **Shift Management**: Create, edit, and track employee shifts
- **Time-off Requests**: Submit and approve vacation/sick leave requests
- **Attendance Tracking**: Clock in/out functionality with real-time monitoring
- **Announcements**: Company-wide communication system
- **Analytics Dashboard**: Overview of staffing metrics and trends
- **Notifications**: Real-time alerts for important events

## Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, shadcn/ui
- **Backend**: Express.js, Node.js
- **State Management**: TanStack Query (React Query)
- **Routing**: Wouter
- **Forms**: React Hook Form with Zod validation
- **Session Management**: Express Sessions
- **Build Tool**: Vite

## Getting Started

### Prerequisites

- Node.js 20 or higher
- npm

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd shiftease-plus
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

### Demo Accounts

Use these credentials to test the application:

- **Admin**: username: `admin`, password: `admin123`
- **Manager**: username: `manager`, password: `manager123`
- **Employee**: username: `employee`, password: `employee123`

## Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run check` - Run TypeScript type checking

## Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Application pages
│   │   ├── hooks/          # Custom React hooks
│   │   └── lib/            # Utility functions
├── server/                 # Backend Express application
│   ├── routes.ts           # API routes
│   ├── storage.ts          # In-memory data storage
│   └── index.ts            # Server entry point
├── shared/                 # Shared types and schemas
│   └── schema.ts           # Database schemas and types
└── package.json
```

## API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user

### Users
- `GET /api/users` - Get all employees
- `POST /api/users` - Create new user
- `GET /api/users/:id` - Get user by ID

### Shifts
- `GET /api/shifts` - Get shifts (with filters)
- `POST /api/shifts` - Create new shift
- `PUT /api/shifts/:id` - Update shift
- `DELETE /api/shifts/:id` - Delete shift

### Time-off Requests
- `GET /api/timeoff` - Get time-off requests
- `POST /api/timeoff` - Submit time-off request
- `PUT /api/timeoff/:id` - Update request status

### Attendance
- `GET /api/attendance` - Get attendance records
- `POST /api/attendance/checkin` - Clock in
- `POST /api/attendance/checkout` - Clock out

### Announcements
- `GET /api/announcements` - Get announcements
- `POST /api/announcements` - Create announcement

### Notifications
- `GET /api/notifications` - Get user notifications
- `GET /api/notifications/unread` - Get unread notifications
- `PUT /api/notifications/:id/read` - Mark as read

## License

MIT License