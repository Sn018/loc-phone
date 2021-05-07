# loc-phone
This program is to find the location, carrier and timezone of the inputted phone number around the world
import phonenumbers
numb=(input("Enter the phone number with country code"))
from phonenumbers import geocoder
country = phonenumbers.parse(numb,"CH")      #using geocoder function from phonenumbers library to get the location
print(geocoder.description_for_number(country,"en"))
from phonenumbers import carrier
service_number = phonenumbers.parse(numb,"RO")
print(carrier.name_for_number(service_number,"en"))     #using carrier function to know the carrier of phone number
from phonenumbers import timezone
zo=phonenumbers.parse(numb)
timezo=timezone.time_zones_for_number(zo)
print(timezo)
