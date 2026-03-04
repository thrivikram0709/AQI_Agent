AQI Simple Reflex Agent
Project Description
This project implements a Simple Reflex Agent that calculates the Air Quality Index (AQI) based on environmental sensor values.
The program takes pollutant values from the user and determines the corresponding air quality category.
The agent behaves like a Simple Reflex Agent in Artificial Intelligence because it directly maps sensor inputs to actions using predefined rules.
________________________________________
Pollutants Used
The system uses four common air pollutants:
•	PM2.5 – Fine particulate matter
•	PM10 – Coarse particulate matter
•	NO2 – Nitrogen dioxide
•	CO – Carbon monoxide
These values are used to estimate the AQI.
________________________________________
AQI Categories
AQI Range	Air Quality Category
0 – 50	Good
51 – 100	Moderate
101 – 150	Unhealthy for Sensitive Groups
151 – 200	Unhealthy
> 200	Hazardous
________________________________________
Program Code
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
________________________________________
How to Run the Program
1.	Install Python 3 on your system.
2.	Save the program as aqi_agent.py.
3.	Open Terminal / Command Prompt.
4.	Run the program using:
python aqi_agent.py
5.	Enter the pollutant sensor values when prompted.
________________________________________
Example Output
Enter sensor values:
PM2.5: 80
PM10: 120
NO2: 60
CO: 1.5

AQI Value: 83.75
Air Quality Category: Moderate
________________________________________
Technologies Used
•	Python 3
________________________________________
AI Concept Used
This project demonstrates the concept of a Simple Reflex Agent, where the agent receives sensor inputs and immediately applies condition–action rules to determine the AQI category.
________________________________________
Group Members
•	P.V. Thrivikram – SE24UCSE051
•	N. Panvitha Reddy – SE24UCSE154
•	N. Jagriti – SE24UCSE140
•	Jiya – SE24UCSE067
________________________________________

