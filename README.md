# Resume Analyzer

A full-stack web application for analyzing and providing feedback on resumes using AI.

## Features

- Upload and analyze PDF resumes
- AI-powered resume analysis and feedback
- Historical resume viewer with detailed analysis
- Modern and responsive UI

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Google Cloud Account (for Gemini API)

## Setup Instructions

### Frontend

1. Navigate to the project root directory
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

### Backend

1. Navigate to the server directory:
   ```bash
   cd server
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Copy `.env.example` to `.env` and update the values:
   ```bash
   cp .env.example .env
   ```
4. Set up PostgreSQL database and update the database connection string in `.env`
5. Run database migrations:
   ```bash
   npx sequelize-cli db:migrate
   ```
6. Start the server:
   ```bash
   npm run dev
   ```

## Environment Variables

Create a `.env` file in the server directory with the following variables:

```
PORT=5000
DB_HOST=localhost
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=resume_analyzer
DB_PORT=5432
GOOGLE_API_KEY=your_google_api_key
```

## Project Structure

```
resume-analyzer/
├── src/                 # Frontend source code
│   ├── components/      # Reusable UI components
│   ├── pages/          # Page components
│   ├── services/       # API and external service integrations
│   └── utils/          # Helper functions
├── server/             # Backend server
│   ├── controllers/    # Business logic
│   ├── routes/         # API endpoints
│   ├── middleware/     # Request handling
│   └── models/         # Database schemas
├── database/           # SQL migrations and seed data
└── config/             # Environment configurations
```

## API Documentation

The backend API provides the following endpoints:

- `POST /api/resume/analyze` - Analyze a resume PDF
- `GET /api/resume/history` - Get all analyzed resumes
- `GET /api/resume/:id` - Get detailed analysis for a specific resume

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

MIT


