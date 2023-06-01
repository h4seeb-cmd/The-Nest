---
layout: post
categories: [ Jekyll, tutorial, web development ]
image: assets/images/2.jpg
---

<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC">
    <style>
        body {
            animation: colorTransition 10s infinite;
            background-color: #87cefa;
        }
@keyframes colorTransition {
            0% { background-color: #87cefa; }
            10% { background-color: #87cefa; }
            20% { background-color: #a4d3ff; }
            30% { background-color: #c1e8ff; }
            40% { background-color: #def3ff; }
            50% { background-color: #ebf9ff; }
            60% { background-color: #f8fdff; }
            70% { background-color: #ebf9ff; }
            80% { background-color: #def3ff; }
            90% { background-color: #c1e8ff; }
            100% { background-color: #a4d3ff; }
        }
.cloud-container {
            position: relative;
        }
.cloud {
            position: absolute;
            width: 200px;
            height: 100px;
            background-color: #fff;
            border-radius: 100px;
            box-shadow: 0px 0px 20px #888888;
            animation: cloudAnimation 10s linear infinite;
            z-index: -1; /* Set a lower z-index to keep the clouds in the background */
        }
.cloud::after,
        .cloud::before {
            content: "";
            position: absolute;
            background-color: #fff;
        }
.cloud::after {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            top: -30px;
            left: 50px;
        }
.cloud::before {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            top: -50px;
            right: 50px;
        }
@keyframes cloudAnimation {
            0% {
                transform: translateX(-200px);
            }
            50% {
                transform: translateX(calc(100% + 200px));
            }
            100% {
                transform: translateX(-200px);
            }
        }
.cloud:nth-child(2) {
            top: 150px;
            left: 200px;
            animation-duration: 15s;
            animation-direction: reverse;
        }
.cloud:nth-child(3) {
            top: 300px;
            left: 500px;
            animation-duration: 12s;
            animation-direction: reverse;
        }
.cloud:nth-child(4) {
            top: 450px;
            left: 800px;
            animation-duration: 10s;
            animation-direction: normal;
        }
.cloud:nth-child(5) {
            top: 600px;
            left: 200px;
            animation-duration: 14s;
            animation-direction: reverse;
        }
.cloud:nth-child(6) {
            top: 750px;
            left: 500px;
            animation-duration: 11s;
            animation-direction: normal;
        }
.title {
            text-align: center;
            font-size: 48px;
        }
.letter {
            display: inline-block;
            animation: bounce 1s infinite alternate, color-change 2s infinite;
        }
@keyframes bounce {
            0% {
                transform: translateY(0);
            }

            100% {
                transform: translateY(-10px);
            }
        }
@keyframes color-change {
            0% {
                color: red;
            }

            25% {
                color: blue;
            }

            50% {
                color: green;
            }

            75% {
                color: orange;
            }

            100% {
                color: purple;
            }
        }
</style>
</head>
<html>
<head>
  <style>
    .myDiv {
      border: 5px outset purple;
      background-color: lightblue;
      text-align: center;
      width: 800px; /* Set the width of the myDiv element */
      margin: 0 auto; /* Center the myDiv element horizontally */
    }
    

  </style>
</head>
<body>
  <div class="cloud-container">
    <div class="cloud"></div>
    <div class="cloud"></div>
    <div class="cloud"></div>
    <div class="cloud"></div>
    <div class="cloud"></div>
    <div class="cloud"></div>
  </div>

  
  
  <div class="gif-container">
    
    <div class="gif-container">
      <img src="https://cdn.dribbble.com/users/261567/screenshots/1099769/googleweather.gif" alt="GIF Image" class="img-fluid" style="width: 1500px; height: 500px;">
    </div>
  </div>

  <div class="myDiv">
    <h2>Welcome to SkySight. With this feature you can find out the weather conditions of any part of the world! Enter either the zip code or the city name and get the data in a blink of an eye.</h2>
  </div>

  <script>
    const letters = document.querySelectorAll('.letter');

    letters.forEach((letter, index) => {
      letter.style.animationDelay = `${index * 0.1}s`;
    });
  </script>
</body>
</html>





<html lang="en">

<head>
  <title>Weather Forecast</title>
  <!-- Add Bootstrap CSS CDN -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
  <style>
    body {
      background-color: #f8f9fa;
    }
.container {
      max-width: 600px;
      margin-top: 50px;
    }
.form-container {
      text-align: center;
      margin-bottom: 20px;
    }
.form-container input {
      width: 100%;
      max-width: 300px;
      border: 1px solid #ced4da;
      border-radius: 4px;
      padding: 6px 12px;
    }
.btn-purple {
      width: 100%;
      max-width: 200px;
      font-size: 18px;
      background-color: #800080;
      color: #fff;
      border: none;
    }
.card {
      background-color: #ffffff;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
      border-radius: 10px;
    }
.table-responsive {
      border: none;
    }
.error-message {
      color: red;
      font-size: 14px;
      margin-top: 10px;
    }
/* Updated CSS for the title */
    .title-container {
      text-align: center;
      animation: bounce 1s infinite;
      font-size: 36px; /* Increased font size for the title */
    }
@keyframes bounce {
      0% {
        color: blue; /* Start color: blue */
      }
      50% {
        color: purple; /* Middle color: purple */
      }
      100% {
        color: blue; /* End color: blue */
      }
    }
  </style>
</head>

<body>
  <div class="container">
    <h1 class="title-container mb-4">Weather Forecast</h1>

<div class="form-container">
      <form id="cityForm">
        <div class="mb-3">
          <input type="text" id="cityInput" class="form-control" placeholder="Enter City" required>
        </div>
        <button type="submit" class="btn btn-purple">Get Forecast</button>
      </form>
    </div>

<div class="form-container">
      <form id="zipForm">
        <div class="mb-3">
          <input type="text" id="zipInput" class="form-control" placeholder="Enter Zip Code" required>
        </div>
        <button type="submit" class="btn btn-purple">Get Forecast</button>
      </form>
    </div>
    

<div class="card d-none">
      <div class="card-body">
        <h5 class="card-title">Weather Forecast</h5>
        <div class="table-responsive">
          <table class="table">
            <thead>
              <tr>
                <th scope="col">Data</th>
                <th scope="col">Value</th>
              </tr>
            </thead>
            <tbody id="weatherData">
              <!-- Table rows for weather forecast will be dynamically added here -->
            </tbody>
          </table>
        </div>
      </div>
    </div>

<div id="errorMessage" class="error-message d-none"></div>
  </div>

  <!-- Add Bootstrap JS CDN -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
  <script>
    function getWeatherForecast(event, locationType) {
      event.preventDefault(); // Prevent form submission
const locationInput = locationType === 'city' ? document.getElementById("cityInput") : document.getElementById("zipInput");
      const location = locationInput.value.trim();
if (location === "") {
        return; // Do nothing if the input is empty
      }
const url = "https://weather-by-api-ninjas.p.rapidapi.com/v1/weather";
      const queryParam = locationType === 'city' ? "city" : "zip";
      const querystring = { [queryParam]: location };
      const headers = {
        "X-RapidAPI-Key": "9e76af0f32msh97501ce28ffe3b8p1c0da6jsnc3113faae226",
        "X-RapidAPI-Host": "weather-by-api-ninjas.p.rapidapi.com"
      };
fetch(url + "?" + new URLSearchParams(querystring), {
          headers: headers
        })
        .then(response => {
          if (!response.ok) {
            throw new Error(response.status); // Handle non-200 status codes as errors
          }
          return response.json();
        })
        .then(data => {
          displayWeatherForecast(data);
          clearErrorMessage();
        })
        .catch(error => {
          console.error("Error:", error);
          displayErrorMessage();
        });
    }
function displayWeatherForecast(data) {
      const resultCard = document.querySelector(".card");
      const weatherData = document.getElementById("weatherData");
// Clear existing table data
      weatherData.innerHTML = "";
// Generate table rows with weather data
      for (const [key, value] of Object.entries(data)) {
        const row = document.createElement("tr");
        const keyCell = document.createElement("td");
        const valueCell = document.createElement("td");
        keyCell.textContent = key;
        valueCell.textContent = value;
        row.appendChild(keyCell);
        row.appendChild(valueCell);
        weatherData.appendChild(row);
      }
// Show the weather forecast card
      resultCard.classList.remove("d-none");
    }
function displayErrorMessage() {
      const errorMessage = document.getElementById("errorMessage");
      errorMessage.textContent = "An error occurred. Please check the location and try again.";
      errorMessage.classList.remove("d-none");
    }
function clearErrorMessage() {
      const errorMessage = document.getElementById("errorMessage");
      errorMessage.textContent = "";
      errorMessage.classList.add("d-none");
    }
// Event listeners for form submissions
    document.getElementById("cityForm").addEventListener("submit", function(event) {
      getWeatherForecast(event, 'city');
    });
document.getElementById("zipForm").addEventListener("submit", function(event) {
      getWeatherForecast(event, 'zip');
    });
  </script>
</body>

</html>
