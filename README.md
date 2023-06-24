# CODE-MAVERICK
Microsoft Hackathon

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
