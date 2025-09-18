# cab-fare
CAB FARE ESTIMATOR
This project provides Python code to calculate the distance between two geographical locations and estimate the final price of a trip based on surge pricing rules determined by the booking hour.

Files
main.py (or the name of your Python file containing the code)
Classes and Functions
Maps Class
This class is used to calculate the distance between two locations.

__init__(self): Constructor for the Maps class.
get_distance(self, location_1, location_2): Calculates the distance between location_1 and location_2 in kilometers. It uses the geopy.distance library for more accurate calculations and falls back to a basic Euclidean distance calculation if geopy encounters an error.
SurgePricing Class
This class is used to determine the price per kilometer based on the booking hour.

__init__(self): Constructor for the SurgePricing class.
get_price_per_km(self, hour): Returns the price per kilometer based on the input hour. It applies surge pricing rules for specific time ranges.
get_final_price(pick_up_location, drop_location, booking_hour) Function
This function calculates the final price of a trip.

pick_up_location: A tuple containing the latitude and longitude of the pick-up location.
drop_location: A tuple containing the latitude and longitude of the drop-off location.
booking_hour: An integer representing the hour of the booking (24-hour format).
This function utilizes the Maps and SurgePricing classes to calculate the total distance and the actual price per kilometer, then returns the rounded final price.

How to Use
Make sure you have the geopy library installed (pip install geopy).
Import the necessary classes and functions from your Python file.
Create instances of the Maps and SurgePricing classes.
Define your pick-up location, drop-off location, and booking hour.
Call the get_final_price() function with the defined locations and hour to get the final price.
