# Provider Service API
## Description
Provider Service API is an API developed with .NET 6 that allows managing tourism service providers. Providers can be airlines, transportation agencies, tour operators, among others. The API enables CRUD operations (Create, Read, Update, Delete) for providers and handles user authentication and authorization using JWT.

## 1. Technologies
.NET 6
Dapper (for database access)
JWT (for authentication)
AutoMapper (for object mapping)
FluentValidation (for validation)
Swagger (for API documentation)
Requirements
.NET 6 SDK
SQL Server
Visual Studio 2022 or higher
Setup and Installation

## 2. Clone the repository:

git clone https://github.com/your-username/ProviderServiceAPI.git
Set up the database:

The API connects to a SQL Server database. Ensure you have a database named ProviderDb. A backup of the database and the "QueryProviderBD" script, which created the tables and stored procedures, are included.

Restore NuGet packages:
From the command line or Visual Studio, run the following command to restore the necessary packages:

dotnet restore

## 3. Run the API:
You can run the API directly from Visual Studio (F5) or from the command line with:

dotnet run


## 4. Main Endpoints
Method	Endpoint	Description
GET	/api/providers	Get all providers
GET	/api/providers/{id}	Get a provider by ID
POST	/api/providers	Create a new provider
PUT	/api/providers/{id}	Update an existing provider
DELETE	/api/providers/{id}	Delete a provider

## 5. Authentication
Authentication is done using JWT. To authenticate, you need to send a login request with valid credentials, and you will receive a JWT token. This token must be included in the headers of subsequent requests.

## 6. Example using Postman:
Make a POST request to /api/auth/login with the user credentials:

{
  "Username": "andrea",
  "Password": "Prueba123"
}
Use the received JWT token in the following requests to access protected endpoints.

## 7. Running Unit Tests
Unit tests are implemented in the ProviderServiceAPI.Tests project.