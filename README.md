# pi_si7021
[![Build Status](https://travis-ci.org/kangasta/pi_si7021.svg?branch=master)](https://travis-ci.org/kangasta/pi_si7021)

Library for playing around with si7021 relative humidity and temperature sensor with Raspberry Pi. Based on [pigpio example](http://abyz.me.uk/rpi/pigpio/examples.html#Python_Si7021_py).

## Usage

```python

from pi_si7021 import Si7021

RHTEMP = Si7021()

print("Temperature: " + str(round(RHTEMP.temperature, 2)) + u" \u00B0C")
print("Relative humidity: " + str(round(RHTEMP.relative_humidity, 2)) + " %")

RHTEMP.close()

```

## Testing

Run unit tests with commands:

```bash
cd pi_si7021

python3 -m unittest discover -s tst/
```

Get test coverage with commands:
```bash
cd pi_si7021

coverage run -m unittest discover -s tst/
coverage report -m
```
