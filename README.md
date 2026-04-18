# Espresso_Water_Tank_Monitor

Here you can find my adaptations to the Espresso Water Tank Monitor from the Adafruit Learning System Guides - https://github.com/adafruit/Adafruit_Learning_System_Guides/tree/main/Espresso_Water_Meter.

I heard about the espresso water meter by John Park on a podcast and decided to build a similar tank level monitor for another espresso machine.
As I had used slightly different components, especially the ultrasonic sensor, I had to make a few adaptations in order to make the project work.

# Changes to settings.toml

Trying to make the project run on a new ESP32-S2-Mini-1, I noticed that no connection could be made with the Adafruit IO. Besides the login credentials, the timezone is a required setting which should match your timezone. I will not post my settings.toml file as it contains WLAN (CIRCUITPY_WIFI_SSID, CIRCUITPY_WIFI_PASSWORD) and Adafruit IO (ADAFRUIT_AIO_USERNAME, ADAFRUIT_AIO_KEY) login credentials, so you need to adapt your settings file to match your setup:

CIRCUITPY_WIFI_SSID = "YOUR_WIFI_SSID"  
CIRCUITPY_WIFI_PASSWORD = "YOUR_WIFI_PWD"  
CIRCUITPY_WEB_API_PASSWORD = "YOUR_WEB_API_PWD"  
CIRCUITPY_WEB_API_PORT = 80  
ADAFRUIT_AIO_USERNAME= "YOUR_AIO_USERNAME"  
ADAFRUIT_AIO_KEY = "YOUR_AIO_KEY"  
TIMEZONE="YOUR_TIMEZONE"  
