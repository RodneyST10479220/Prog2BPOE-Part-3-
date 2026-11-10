# RaceDay SA

## Project Overview

RaceDay SA is a sports event and race management system designed to help users manage and interact with racing events.

The system allows users to register and log in to the application, view and manage their profiles, and interact with racing events. The project consists of two separate ASP.NET Core applications:

- An ASP.NET Core Web API
- An ASP.NET Core MVC application

The MVC application acts as the user interface and communicates with the Web API using HTTP requests. The MVC application does not directly access the database. All database operations and business logic are handled by the API.

## System Architecture

The project follows an API-driven architecture.

The flow of the application is:

MVC Application → Web API → Database

The MVC application sends requests to the Web API using `HttpClient`. The API processes the requests, performs the required database operations, and returns responses to the MVC application.

This approach separates the user interface from the database and business logic.

## Technologies Used

The project was developed using:

- C#
- ASP.NET Core Web API
- ASP.NET Core MVC
- SQL Server
- Entity Framework Core
- HTML
- CSS
- JavaScript
- HTTP Client
- Swagger

## Web API

The Web API is responsible for handling the application's data and database operations.

The API manages functionality such as:

- User registration
- User login
- User profile retrieval
- User profile updates
- Creating events
- Retrieving events
- Updating events
- Managing event information

The API communicates with the SQL Server database and returns data to the MVC application.

Swagger can be used to test and interact with the available API endpoints.

## MVC Application

The MVC application provides the user interface for RaceDay SA.

Instead of directly connecting to the database, the MVC application communicates with the Web API using `HttpClientFactory`.

The MVC application is responsible for:

- Displaying the RaceDay SA homepage
- Providing registration functionality
- Providing login functionality
- Displaying user profile information
- Displaying event information
- Creating events
- Updating event information
- Providing a user-friendly interface for interacting with the system

## User Registration

Users can create an account by providing the required registration information.

The MVC application sends the registration information to the Web API. The API processes the request and stores the user's information in the database.

After successful registration, the user can access their profile.

## User Login

Existing users can log into the system using their account details.

The MVC application sends the login information to the Web API for validation. The API checks the user's information and returns the appropriate response.

After successful authentication, the user can access the relevant features of the system.

## User Profile

The application includes a user profile section where users can view their account information.

The profile functionality retrieves user information through the Web API instead of accessing the database directly.

Users can also update their profile information through the system.

## Event Management

RaceDay SA allows users to interact with racing events.

The event functionality includes:

- Viewing available events
- Viewing detailed event information
- Creating new events
- Updating event information
- Accessing event action buttons

The MVC application retrieves event data from the Web API.

## Event Display

Events are displayed in the MVC application in an organised format.

The event interface includes collapsible sections that allow users to view an event name and expand it to see additional event details.

This helps keep the interface clean while still allowing users to access the full information about each event.

## Create Event

The Create Event functionality allows users to enter information for a new racing event.

The MVC application collects the event information and sends it to the Web API.

The Web API processes the request and performs the required database operation.

## Update Event

The project includes an Update Event interface.

Users can access event information and interact with the available update functionality through the MVC application.

The MVC application communicates with the Web API to handle event-related operations.

## Database

The database is managed through the Web API.

The MVC application does not contain direct database access.

This means that database connections, SQL operations, and business logic are handled by the API, while the MVC project focuses on displaying information and providing the user interface.

## Project Structure

The project consists of two main applications.

### API Project

The API project contains:

- Models
- Controllers
- Database configuration
- API endpoints
- User functionality
- Event functionality
- Database operations

### MVC Project

The MVC project contains:

- Controllers
- Views
- HTML and CSS
- User interface functionality
- `HttpClient` communication with the API

## API Communication

The MVC application uses `HttpClientFactory` to communicate with the Web API.

The general process works as follows:

1. A user interacts with the MVC application.
2. The MVC controller receives the request.
3. The MVC application sends an HTTP request to the Web API.
4. The API processes the request.
5. The API communicates with the database when necessary.
6. The API returns a response.
7. The MVC application displays the result to the user.

## How to Run the Project

### Requirements

Before running the project, make sure the following software is installed:

- Visual Studio
- SQL Server or SQL Server LocalDB
- .NET SDK compatible with the project

### Running the API

1. Open the API project in Visual Studio.
2. Ensure the database connection is correctly configured.
3. Run the API project.
4. Confirm that the API is running successfully.
5. Swagger can be used to test the API endpoints.

### Running the MVC Application

1. Open the MVC project in Visual Studio.
2. Ensure that the API base URL is correctly configured.
3. Make sure the Web API is running.
4. Run the MVC application.
5. Open the application in the browser.

The MVC application will communicate with the Web API to retrieve and manage data.

## Key Design Principle

A key requirement of the project is the separation between the MVC application and the database.

The MVC application:

- Does not directly access the database.
- Does not contain duplicated database logic.
- Uses HTTP requests to communicate with the API.

The Web API is responsible for:

- Database access
- Data processing
- Application logic
- Returning responses to the MVC application

## Future Improvements

Possible future improvements include:

- Completing full event update functionality
- Completing event deletion functionality
- Adding event categories
- Adding participant enrolment functionality
- Adding race results
- Adding authentication and authorisation improvements
- Improving error handling
- Improving validation
- Adding additional responsive design features

## Conclusion

RaceDay SA is an API-driven sports event management system built using ASP.NET Core technologies.

The project demonstrates the separation of responsibilities between an ASP.NET Core Web API and an ASP.NET Core MVC application. The API manages data and database operations, while the MVC application provides the user interface and communicates with the API through HTTP requests.

This architecture creates a structured and maintainable approach to building a full-stack web application.
