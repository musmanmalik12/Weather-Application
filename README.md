# Weather Dashboard

This project is a full-stack web application that displays current weather data, including daily and hourly weather details based on user input. It also features authentication with JWT tokens for user login and signup, with tokens stored in cookies for secure session handling.

## Features

### Frontend
- Built using **React**.
- User Authentication with:
  - **Login** and **Signup** forms.
  - **JWT** tokens for authentication.
  - **bcrypt** for password hashing.
  - **Cookies** for secure token storage.
- Displays:
  - **Current day's weather data**.
  - **Hourly weather details** for the selected date.

### Backend
- Developed with **Node.js** and **Express**.
- **Prisma ORM** for managing **MySQL** database operations.
- **Weather API** integration to fetch weather data.
- Secure authentication using **JWT**.

## Getting Started

### Prerequisites

- **Node.js**: Make sure you have Node.js installed on your machine.
- **MySQL Database**: Set up a MySQL database and update the connection details in Prisma's configuration file.
- **Weather API Key**: You will need an API key from a weather service provider (e.g., OpenWeatherMap).

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/weather-dashboard.git
   cd weather-dashboard
Install dependencies: For both frontend and backend, install the required dependencies using:

bash
Copy code
npm install
Set up environment variables:

In the WeatherAPI.js file, replace YOUR_API_KEY_HERE with your actual weather API key.
In the Auth.js file, replace YOUR_SECRET_KEY_HERE with your JWT secret key.
For example:

javascript
Copy code
// WeatherAPI.js
const API_KEY = "YOUR_API_KEY_HERE";

// Auth.js
const JWT_SECRET = "YOUR_SECRET_KEY_HERE";
Run database migrations: Ensure that your Prisma setup is connected to the MySQL database:

bash
Copy code
npx prisma migrate dev
Start the backend server:

bash
Copy code
npm start
Start the frontend: Navigate to the client folder and start the React application:

bash
Copy code
cd client
npm start
Usage
Login/Signup: Use the login and signup forms to create an account and log in to the application. Passwords are hashed using bcrypt, and upon successful login, a JWT token will be stored in cookies.
Weather Search: After logging in, you can search for a city to get the current weather and hourly details for the day.
File Structure
client/: Contains the React frontend code.
server/: Contains the Node.js backend code.
src/routes/WeatherAPI.js: File where the weather API key needs to be added.
src/routes/Auth.js: File where the JWT secret key needs to be added.
Environment Variables
You will need to define the following environment variables:

Variable	Description
API_KEY	Your weather API key
JWT_SECRET	Your secret key for JWT
DATABASE_URL	Prisma connection string
Technologies Used
Frontend: React
Backend: Node.js, Express
Database: MySQL (managed using Prisma ORM)
Authentication: JWT, bcrypt, cookies
Weather API: For fetching weather data
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
Weather data is provided by OpenWeatherMap.
Prisma ORM documentation can be found here.
