# LabEquipmentApi

## Overview
LabEquipmentApi is a REST API for managing laboratory equipment. It allows users to retrieve equipment records, add new equipment, update existing records, delete equipment, view available equipment, and see equipment summaries by room.

## Technologies Used
- ASP.NET Core Web API
- C#
- Entity Framework Core
- PostgreSQL
- Npgsql
- FluentValidation
- Mapster

## Features
- Retrieve all equipment
- Retrieve equipment by ID
- Create new equipment
- Update equipment
- Delete equipment
- Retrieve available equipment
- View equipment statistics by room
- Validate equipment creation requests

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/equipment` | Retrieve all equipment |
| GET | `/api/equipment/{id}` | Retrieve equipment by ID |
| POST | `/api/equipment` | Create equipment |
| PUT | `/api/equipment/{id}` | Update equipment |
| DELETE | `/api/equipment/{id}` | Delete equipment |
| GET | `/api/equipment/available` | Retrieve available equipment |
| GET | `/api/equipment/room-summary` | Retrieve equipment summary by room |

## Database

The project uses PostgreSQL with Entity Framework Core.

The database connection is configured through the `LabDbConnection` connection string.

## Running the Project

1. Open the project in Visual Studio.
2. Configure the PostgreSQL connection string.
3. Restore NuGet packages.
4. Apply the database migrations if necessary.
5. Run the application.

## Project Structure

- `Controllers` – API endpoints
- `Contracts` – Request and response models
- `Data` – Database context
- `Domain` – Equipment entity
- `Migrations` – Database migration files
- `Properties` – Application launch settings

## Development

This project follows a layered structure to separate API controllers,
data access, domain models, and request contracts.

The API uses dependency injection to manage services and database
dependencies.

## API Usage

The API can be accessed through HTTP requests using tools such as Swagger UI, Postman, or curl.

Clients can use the available endpoints to manage laboratory equipment and retrieve equipment information.