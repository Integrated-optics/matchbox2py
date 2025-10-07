# matchbox2py

Python library for controlling Integrated Optics MatchBox2 laser modules via USB serial communication.

---

## Features

- Connect and communicate with MatchBox 2 devices
- Read device information and settings
- Send commands and parse responses
- Structured models for laser info, readings, and settings

---

##  Installation

You can install the library directly from GitHub:

```bash
pip install git+https://github.com/Integrated-optics/matchbox2py.git@master#egg=matchbox2
```

Alternatively, you can add this line to your `requirements.txt`:

```
git+https://github.com/Integrated-optics/matchbox2py.git@master#egg=matchbox2
```

and install all dependencies with:

```bash
pip install -r requirements.txt
```

---

## Usage Example

```python
from matchbox2py.matchbox2 import MatchBox2Laser

# List all available connected lasers
lasers = MatchBox2Laser().get_available_lasers()
print("Detected lasers:", lasers)

# Connect to the first available laser
if lasers:
    laser = MatchBox2Laser()
    laser.connect("COM3")
    # Turn the laser on
    laser.set_laser_on()
    # Turn the laser off
    laser.set_laser_off()
else:
    print("No lasers detected.")
```

---
## Links

- **Homepage:** [https://integratedoptics.com](https://integratedoptics.com)  
- **Repository:** [https://github.com/Integrated-optics/matchbox2py](https://github.com/Integrated-optics/matchbox2py)




