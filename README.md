# CODE-MAVERICK
Microsoft Hackathon
# Weather Forecasting Tool

The Weather Forecasting Tool is a command line tool that accepts a city's name as input and returns the current weather forecast. It leverages the OpenWeatherMap API to fetch weather data and parse it using Python.

## Usage of GITHUB COPILOT

GitHub Copilot was used in this code to help use write the " get_weather_forecast() function".  Copilot suggested the following code:


def get_weather_forecast(city):
    url = "https://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}".format(
        city=city,
        api_key="d8957090639963e556861ce83d35b1b0"
    )
    response = requests.get(url)
    if response.status_code == 200:
        data = json.loads(response.content)
        return data
    else:
        return None


-->GITHUB Copilot suggested the following code to  print the weather data:


if weather_data:
        print("Current weather for {}:".format(city))
        print("Temperature: {}°C".format(weather_data["main"]["temp"]))
        print("Humidity: {}%".format(weather_data["main"]["humidity"]))
        print("Pressure: {}hPa".format(weather_data["main"]["pressure"]))
    else:
        print("Could not find weather data for {}.".format(city))

 In this case, Copilot helped in writing the get_weather_forecast() function and print the weather data.
# basically github copilot was used in several parts in this code:
-->Import Statements:Copilot can suggest the import statements for the requests and json modules based on their common usage in API requests and JSON parsing.

-->API URL and String Formatting:Copilot can assist in generating the API URL string by suggesting the format and placeholders for the city and API key values. For example, it might suggest using the .format() method to insert the values into the URL string.

-->HTTP Request and Error Handling:Copilot can provide suggestions for making the HTTP request using the requests.get() method and help with error handling. It might recommend checking the status code (response.status_code) and returning None if it's not 200.

-->JSON Parsing:Copilot can assist with parsing the JSON response by suggesting the usage of json.loads() to convert the response content into a Python dictionary.

-->User Input and Output:Copilot can help with generating the code to prompt the user for input using input(). It might also suggest the format and placeholders for displaying the weather information using print().

# THE ARCHITECTURAL FLOW OF THE CODE IS:

Weather Forecast CLI Tool

This command line tool accepts a city name as input and returns the current weather forecast for that city. It leverages the OpenWeatherMap API to fetch weather data and parses it using Python.

# Architecture Flow:

1. User Input:
   - The tool prompts the user to enter a city name through the command line.

2. API Request:
   - The city name provided by the user is used to construct an API URL for the OpenWeatherMap API.
   - The tool makes an HTTP GET request to the API URL using the `requests` module.
   - If the API request is successful (HTTP status code 200), the response content is obtained.

3. Data Parsing:
   - The response content, in JSON format, is parsed using the `json` module's `loads()` function.
   - The parsed data is stored in a Python dictionary.

4. Data Display:
   - If the weather data dictionary is not empty, the tool displays the current weather information for the city.
   - The temperature, humidity, and pressure are extracted from the weather data dictionary and printed on the command line.
   - If the weather data dictionary is empty, a message is displayed indicating that weather data for the city could not be found.

Usage:

1. Install Dependencies:
   - Ensure that Python is installed on your system.
   - Install the `requests` module by running `pip install requests` in your terminal.

2. Obtain an API Key:
   - Sign up on the OpenWeatherMap website to obtain an API key.
   - Replace `"YOUR_API_KEY"` in the Python code with your actual API key.

3. Run the Tool:
   - Open a terminal and navigate to the directory where the Python script is located.
   - Run the script by executing the command `python weather_forecast.py`.
   - Enter the name of the city for which you want to retrieve the weather forecast.
   - The tool will display the current weather information if available.

Note: The tool uses the metric system for temperature (°C) and pressure (hPa).


