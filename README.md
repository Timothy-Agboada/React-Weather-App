## 🚀 30-Day Coding Challenge: Day 24

This project is the twenty-fourth entry in my 30-day coding challenge. Today's goal was to rebuild and enhance the Weather App from Day 12 using React. This exercise demonstrates the power of React for managing complex UI states, handling multiple API calls, and creating a more robust and maintainable application.

### 📖 Project Overview

This is a full-featured weather forecast application built with React. Users can search for any city, and the app will display the current weather conditions along with a 5-day forecast. It includes a toggle switch to seamlessly change all temperature units between Celsius and Fahrenheit, which automatically re-fetches the data to ensure accuracy. The application handles loading and error states gracefully to provide a smooth user experience.

### ✨ Live Demo & Screenshot

Below is a screenshot of the application's interface.
![Jul-02-2025 17-47-51](https://github.com/user-attachments/assets/fdc57b95-de96-49ff-ba43-38af5d948866)


### 🌟 Key Features

* **Current Weather & 5-Day Forecast:** Displays a comprehensive weather overview.
* **Celsius/Fahrenheit Toggle:** A unit toggle switch allows users to change temperature units, which instantly updates all displayed data.
* **Multi-Step API Fetching:** Implements a robust two-step fetch process: first to get a city's coordinates, then to get the weather data.
* **Parallel API Calls:** Uses `Promise.all` to fetch current weather and forecast data simultaneously for better performance.
* **Stateful UI:** Built with React, where the UI is a direct reflection of the application's state (loading, error, weather data, units).
* **Component-Based Architecture:** The UI is broken down into logical components (`CurrentWeatherCard`, `ForecastCard`) for better organization.
* **Modern & Responsive Design:** A clean, visually appealing interface styled with Tailwind CSS that works great on all devices.

### 💻 Technologies Used

This project was built using a modern, lightweight React setup.

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Babel](https://img.shields.io/badge/Babel-%23F9DC3e.svg?style=for-the-badge&logo=babel&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

* **React:** The core library for building the user interface and managing state.
* **ReactDOM:** Used to render the React component into the browser's DOM.
* **Babel:** Used as a transpiler to convert JSX into standard JavaScript.
* **Tailwind CSS:** For all styling and layout.
* **OpenWeatherMap API:** The source for all weather data.
* **Font Awesome:** For icons.

### 🛠️ How to Run Locally

This project requires an API key from OpenWeatherMap to function.

1.  **Get a free API Key** from [OpenWeatherMap](https://openweathermap.org/).
2.  **Clone the repository (or download the code):**
    ```bash
    git clone https://github.com/timothy-agboada/react-weather-app.git
    ```
3.  **Navigate to the project directory:**
    ```bash
    cd react-weather-app
    ```
4.  **Add your API Key:**
    * Open the `index.html` file.
    * Inside the `<script type="text/babel">` tag, find the line `const API_KEY = 'YOUR_API_KEY';`
    * Replace `'YOUR_API_KEY'` with your actual key.
5.  **Open the `index.html` file in your web browser.**

### 🎯 Learning Objectives

This project was a comprehensive review and extension of key React concepts:

* **Refactoring with React:** Understanding the benefits of React's declarative, state-driven approach compared to imperative vanilla JavaScript for building the same application.
* **Advanced `useEffect`:** Using the `useEffect` hook with multiple dependencies (`[cityToFetch, units]`) to automatically trigger data re-fetching when either the city or the units change.
* **Complex State Management:** Juggling multiple pieces of state (`city`, `units`, `weatherData`, `loading`, `error`) to manage the complete lifecycle of the application.
* **Handling API Errors:** Building a more robust `try...catch` block to handle various potential failure points in a multi-step API process.
* **Processing API Data:** Writing logic to parse and filter API data into a format suitable for display (e.g., getting one forecast per day from a 3-hour list).

