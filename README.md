# Vehicle Occlusion Detection App

A full-stack application for detecting vehicle occlusions using machine learning models.

## Project Structure

- **Frontend**: React-based UI served on port 3000
- **Backend**: Node.js/Express API on port 5002
- **Database**: Local file-based storage (JSON files)
- **ML Models**: Vehicle detection and occlusion analysis

## Quick Start

### Prerequisites
- Node.js (v14+)
- npm or yarn

### Running Locally

1. **Start Backend**:
   ```bash
   cd backend
   node src/server.js
   ```
   Backend runs on: `http://localhost:5002`

2. **Start Frontend** (in another terminal):
   ```bash
   cd frontend
   npx serve -s build -l 3000
   ```
   Frontend runs on: `http://localhost:3000`

3. **Access the App**:
   - Open `http://localhost:3000` in your browser
   - Register or login to access the dashboard

## API Endpoints

- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/upload` - Upload vehicle images
- `GET /api/detection` - Get detection results
- `GET /api/health` - Health check endpoint

## Features

- User authentication (register/login)
- Image upload for vehicle detection
- Real-time detection results
- Detection history tracking
- User profile management

## Development

### Backend Structure
```
backend/
├── src/
│   ├── server.js           # Express app setup
│   ├── middleware/         # Auth, error handling
│   ├── routes/             # API routes
│   ├── models/             # Data models
│   ├── services/           # Business logic
│   └── utils/              # Utility functions
├── data/                   # Local JSON data storage
└── package.json
```

### Frontend Structure
```
frontend/
├── src/
│   ├── pages/              # Page components
│   ├── components/         # Reusable components
│   ├── context/            # React Context (Auth)
│   ├── services/           # API services
│   └── App.js              # Main app component
├── public/                 # Static assets
└── package.json
```

## Environment Variables

Create `.env` in backend directory:
```
PORT=5002
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
```

## Docker

To run with Docker Compose:
```bash
docker-compose up
```

## License

Proprietary - Vehicle Occlusion Detection System
