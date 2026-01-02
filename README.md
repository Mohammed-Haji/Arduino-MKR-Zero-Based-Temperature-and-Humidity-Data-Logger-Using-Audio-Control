# Arduino-MKR-Zero-Based-Temperature-and-Humidity-Data-Logger-Using-Audio-Control

This project utilizes an Arduino MKR Zero to create a hands-free environmental data logger that records temperature and humidity readings from a DHT11 sensor directly to the onboard SD card. By integrating a digital sound sensor, the system eliminates the need for physical buttons, allowing users to toggle the logging process on or off simply by clapping. When active, the device captures timestamped data every two seconds and saves it to a datalog.txt file in a CSV-compatible format, automatically marking the start and stop times of each session to facilitate easy data analysis and export.

How to use it, let's break down:

Cheack Figure 1

[ Audio Sensor ] ─────( D0 -> Pin 6 )─────┐
                                          │
                                          v
                                 [ Arduino MKR Zero ] ──────> [ SD Card ]
                                          ^       │
                                          │       └─────────> [ Timer Counter (TC) ]
[ DHT11 Sensor ] ─────( Data -> Pin 7 )───┘

Note: You can use other PIN numbers 
