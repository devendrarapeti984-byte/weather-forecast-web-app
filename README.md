# weather-forecast-web-app
A responsive real-time weather forecast web application built using HTML, CSS, JavaScript, and OpenWeatherMap API to display live weather information for multiple locations.

Problem Statement:

Many users face difficulty in accessing accurate and real-time weather information quickly for different locations. Traditional weather platforms may contain complex interfaces and unnecessary information. There is a need for a simple, responsive, and user-friendly web application that provides live weather updates instantly using external weather APIs.

Solution:

To solve this problem, a Real-Time Weather Forecast Web Application was developed using HTML, CSS, and JavaScript integrated with the OpenWeatherMap API. The application allows users to enter any city name and instantly fetches real-time weather details such as temperature, humidity, wind speed, and weather conditions. The system uses asynchronous API calls and dynamic content rendering to provide accurate weather information through a responsive and interactive user interface.


Project Overview:

The Weather Application is a web-based application developed to provide real-time weather information for different cities using a weather API. Users can search for any location and view weather details such as temperature, humidity, wind speed, and weather conditions.

Objective of the Project:

The main objective of this project is:
--To fetch live weather data from an external API
--To display weather information in a user-friendly interface
--To improve frontend and API integration skills
--To understand real-time data handling in web development

Technologies Used:

-> Frontend	: HTML, CSS, JavaScript

->API:	OpenWeatherMap API

->Styling :	CSS / Bootstrap

->Deployment :	Netlify / GitHub Pages


Features of the Weather Application:

1. City Search Functionality
Users can enter a city name to get weather information.
Example:
Input: Hyderabad
2. Real-Time Weather Data
The application fetches:
Temperature
Humidity
Wind speed
Weather condition
Country name
3. Dynamic User Interface
Weather information updates dynamically without refreshing the page.
4. Error Handling
Displays messages for:
Invalid city names
Network errors
API failures
5. Responsive Design
Works on:
Mobile devices
Tablets
Desktop systems

Working Process of the Project:

"Step-by-Step Workflow"
User enters city name

          ↓
Frontend sends API request

          ↓
Weather API returns JSON data

          ↓
JavaScript processes data

          ↓
Weather details displayed on screen


API Used:
OpenWeatherMap API
The API provides real-time weather data in JSON format.

Example API Request
fetch(`https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=YOUR_API_KEY&units=metric`)

Example JSON Response
{
  "name": "Hyderabad",
  "main": {
    "temp": 32,
    "humidity": 60
  },
  "wind": {
    "speed": 5.2
  },
  "weather": [
    {
      "main": "Clouds"
    }
  ]
}
Frontend Explanation
HTML

Used to create:

Search box
Buttons
Weather display cards
CSS

Used for:

Styling
Responsive layout
Attractive UI design
JavaScript

Handles:

API calls
Data fetching
DOM manipulation
Dynamic updates
Sample Functionalities
Search Weather

async function getWeather(city) {
    const response = await fetch(apiUrl + city + `&appid=${apiKey}`);
    const data = await response.json();

    document.querySelector(".temp").innerHTML = data.main.temp + "°C";
}

Challenges Faced:

Handling invalid city names
Managing asynchronous API calls
Designing responsive UI
Parsing JSON data
