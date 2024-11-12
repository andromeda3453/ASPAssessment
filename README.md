
# ASP.NET Core Web API project with JWT Authentication

### Project Overview
This is an ASP.NET Core Web API project that implements user authentication using JWTs. It uses Entity Framework Core in a Code-First approach and incorporates ASP.NET Identity for user management. The project is structured to follow the Repository Pattern for a clean and maintainable architecture.

### Project Setup

#### There are some prerequisites to be able to run this project:
* .NET 6 or later
* MS SQL Server

&nbsp;
#### Code Setup:

#### 1. Configure Database Connection
Update the  **appsettings.json**  file with your SQL Server connection string 

#### 2. Configure JWT Secret Key
Set a JWT Secret Key in the **secrets.json** file

#### 3. Run database migration commands to setup database
```console
dotnet ef migrations add InitialCreate
dotnet ef database update
```


&nbsp;
### Testing the Application

#### You can test the application using the Swagger UI. Launch the project and go to the default swagger url **https://localhost:[port]/swagger/index.html**, Where port is the port number that the app is running on.


&nbsp;
### API Endpoints

#### The app contains 2 endpoints. One for User registration and one for User Login

### User registration:
* Endpoint: _POST /api/User/Register_
* Description: Registers a new user.
* Request Body:
```json
{
  "email": "user@example.com",
  "password": "YourPassword123!",
  "confirmPassword": "YourPassword123!"
}
```
[Sample Request and Response](https://github.com/andromeda3453/ASPAssessment/blob/master/User%20Registration.jpeg)

### User Login:
* Endpoint: _POST /api/User/Login_
* Description: Logs in an existing user.
* Request Body:
```json
{
  "email": "user@example.com",
  "password": "YourPassword123!",
}
```
[Sample Request and Response](https://github.com/andromeda3453/ASPAssessment/blob/master/User%20Login.jpeg)


