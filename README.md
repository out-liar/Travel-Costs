# Travel-Costs.py
# This Python code helps calculate costs while travelling: my first small project.
#
# The code begins here:

# Hotel cost calculator
def hotel_cost(nights):
  return 140*nights

# Plane ticket calculator for selected destination
def plane_ride_cost(city):
  if city == "Charlotte":
   return 183
  elif city == "Tampa":
   return 220
  elif city == "Pittsburgh":
   return 222
  elif city == "Los Angeles":
   return 475
  else:
    print "Select valid destination"

# Rental car calulator
def rental_car_cost(days):
  cost = 40 * days
  if days >= 7:
    cost -= 50
  elif days >= 3:
    cost -= 20
  return cost

# Trip cost total, including spending money
def trip_cost(city, days, spending_money):
  return rental_car_cost(days) + hotel_cost(days-1) + plane_ride_cost(city) + spending_money

# Input travel details: ( city, days, spending money)
print trip_cost("Los Angeles", 5, 600)

# Calculator coded by out_liar consulting
