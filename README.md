# CODE-MAVERICK
Microsoft Hackathon
# Weather Forecasting Tool

The Weather Forecasting Tool is a command line tool that accepts a city's name as input and returns the current weather forecast. It leverages the OpenWeatherMap API to fetch weather data and parse it using Python.

## Usage

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


Copilot suggested the following code to  print the weather data:


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
