# InkwireForms
A modern survey and polling platform with conditional logic, question branching, and real-time analytics. Built with Go backend for handling survey creation, response collection, result aggregation, and multi-format exports.

## Features

1. Multiple question types (multiple choice, text, rating scales, matrix)
2. Conditional logic and question branching
3. Anonymous and authenticated response modes
4. Real-time result aggregation and analytics
5. Export to CSV, Excel, and JSON
6. Role-based access control and survey sharing

## Tech Stack

- Backend: Go 1.21+
- Database: PostgreSQL
- Authentication: JWT tokens
- API: RESTful

## Getting Started

#### Prerequisites:
- Go 1.21+
- PostgreSQL 14+

### Installation:
--------
#### *Clone the repository:*
HTTPS:
```
git clone https://github.com/krosengr4/inkwire-query.git
```
SSH:
```
git clone git@github.com:krosengr4/inkwire-query.git
```

#### *Install dependencies:*
- go mod download

#### *Set up environment variables:*
- cp .env.example .env

#### *Start the server:*
```
go run cmd/server/main.go
```
- The API will be available at http://localhost:8080

### API Endpoints
- POST /api/v1/surveys - Create survey
- GET /api/v1/surveys - List surveys
- GET /api/v1/surveys/:id - Get survey details
- PUT /api/v1/surveys/:id - Update survey
- DELETE /api/v1/surveys/:id - Delete survey

Responses

- POST /api/v1/surveys/:id/responses - Submit response
- GET /api/v1/surveys/:id/responses - Get all responses
- GET /api/v1/surveys/:id/results - Get aggregated results

## Project Structure
```mermaid
inkwireforms/
├── cmd/
│   ├── server/       # Main application entry point
│   └── migrate/      # Database migrations
├── internal/
│   ├── api/          # HTTP handlers and routing
│   ├── models/       # Data models
│   ├── service/      # Business logic
│   └── repository/   # Database layer
├── pkg/
│   └── middleware/   # Reusable middleware
└── migrations/       # SQL migration files
```

## Contributing
- Report a bug or a feature you would like to see implemented [here](https://github.com/krosengr4/inkwire-query/issues)

## License
- MIT License
- For more information about the license, please follow this link: https://opensource.org/license/mit/