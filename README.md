# 🌤️ Go Weather API

A simple Go application that returns current weather data for a given city using the OpenWeatherMap API.

## 📦 Features

- `/hello` endpoint returns a static greeting.
- `/weather/{city}` returns the current weather data for the given city.
- Parses JSON response from OpenWeatherMap and extracts relevant fields.
- Loads API key securely from a config file.

Configuration
Create a .apiConfig file in the root directory with the following JSON content:

{
  "OpenWeatherMapApiKey": "YOUR_API_KEY_HERE"
}
Replace YOUR_API_KEY_HERE with your actual OpenWeatherMap API key.

Run the App

go run main.go

The server will start on:
http://localhost:8080

Endpoints
GET /hello
Returns a basic greeting.

curl http://localhost:8080/hello
Response:

hello from go

GET /weather/{city}
Returns weather data for the given {city}.

Example:

curl http://localhost:8080/weather/London
Sample JSON Response:

{
  "name": "Delhi",
  "main": {
    "temp": 289.82
  }
}
Temperature is in Kelvin.


