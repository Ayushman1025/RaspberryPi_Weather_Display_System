# RaspberryPi_Weather_Display_System


This project uses a Raspberry Pi to interface with multiple sensors, including a DHT11 sensor for temperature and humidity, a light-dependent resistor (LDR) for light intensity, and an analog rain sensor. The project displays real-time data on an I2C LCD screen.

## Project Overview

The goal of this project is to create a simple weather monitoring system that reads environmental data and displays it on an LCD screen. It continuously monitors the following:

- **Temperature (°C and °F)**: Read from the DHT11 sensor.
- **Humidity (%)**: Also read from the DHT11 sensor.
- **Light Intensity**: Measured using an LDR.
- **Rain Detection**: Measured using an analog rain sensor.

The data is displayed on an LCD, and the system also prints the readings to the terminal.

## Features

- Real-time temperature and humidity monitoring.
- Light detection (High/Low light levels).
- Rain sensor to detect the presence of rain.
- LCD display for displaying sensor values.
- Python-based implementation with easy-to-understand code.

## Components Used

- **Raspberry Pi** (Any model with GPIO pins)
- **DHT11 Sensor** (For temperature and humidity)
- **LDR (Light Dependent Resistor)** (For light intensity)
- **Analog Rain Sensor** (For rain detection)
- **I2C LCD Display** (For showing sensor readings)

## Wiring Diagram

- **DHT11 Sensor**: Connect the DHT11 sensor to GPIO pin 17.
- **LDR**: Connect one end to GPIO pin 27 and the other end to ground.
- **Rain Sensor**: Connect to the I2C bus (SDA and SCL).
- **LCD Display**: Connect via I2C to the Raspberry Pi's SDA and SCL pins.

## Software Requirements

- Python 3.x
- Required Python libraries:
  - `adafruit_dht` (for DHT11 sensor)
  - `RPi.GPIO` (for GPIO pin control)
  - `smbus` (for I2C communication)
  - `time` (for delays)
  - `I2C_LCD_driver` (for interfacing with the LCD)

Install required libraries using pip:
```bash
pip install adafruit-circuitpython-dht
pip install RPi.GPIO
pip install smbus
