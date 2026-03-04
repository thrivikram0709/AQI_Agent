def calculate_aqi(pm25, pm10, no2, co):

    aqi = (pm25 + pm10 + no2 + co*50) / 4

    if aqi <= 50:
        category = "Good"
    elif aqi <= 100:
        category = "Moderate"
    elif aqi <= 150:
        category = "Unhealthy for Sensitive Groups"
    elif aqi <= 200:
        category = "Unhealthy"
    else:
        category = "Hazardous"

    return aqi, category


def simple_reflex_agent():

    print("Enter sensor values:")

    pm25 = float(input("PM2.5: "))
    pm10 = float(input("PM10: "))
    no2 = float(input("NO2: "))
    co = float(input("CO: "))

    aqi, category = calculate_aqi(pm25, pm10, no2, co)

    print("\nAQI Value:", round(aqi,2))
    print("Air Quality Category:", category)


simple_reflex_agent()