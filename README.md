# Anniversaries
The 'anniversaries' component is a Home Assistant custom sensor which counts down to a recurring date such as birthdays, but can be used for any anniversary which occurs annually on the same date.

State Returned:
* The number of days remaining to the next occurance.

Attributes:
* years at next anniversary: number of years that will have passed at the next occurrence 
* current years: number of years have passed since the first occurance (ie, age)
* date:  The date as configured

## Table of Contents
* [Installation](#installation)
  + [Manual Installation](#manual-installation)
  + [Installation via HACS](#installation-via-hacs)
* [Configuration](#configuration)
  + [Configuration Parameters](#configuration-parameters)
* [State and Attributes](#state-and-attributes)

## Installation

### MANUAL INSTALLATION
1. Download the
   [latest release](https://github.com/pinkywafer/anniversaries/releases/latest).
2. Unpack the release and copy the `custom_components/anniversaries` directory
   into the `custom_components` directory of your Home Assistant
   installation.
3. Configure the `anniversaries` sensor.
4. Restart Home Assistant.

### INSTALLATION VIA HACS
1. Ensure that [HACS](https://custom-components.github.io/hacs/) is installed.
2. Search for and install the "anniversaries" integration.
3. Configure the `anniversaries` sensor.
4. Restart Home Assistant.

## Configuration
Add `anniversaries` sensor in your `configuration.yaml`. The following example adds two sensors - Shakespeare's birthday and wedding anniversary!
```yaml
# Example configuration.yaml entry
sensor:
  - platform: anniversaries
    name: Shakespeare's Birthday
    date: '1564-04-23'
  - platform: anniversaries
    name: Shakespeare's Wedding Anniversary
    date: '1582-11-27'
```

### CONFIGURATION PARAMETERS
|Attribute |Optional|Description
|:----------|----------|------------
|`platform` | No |`anniversaries`
|`date` | No | date in format `'YYYY-MM-DD'`
| `icon_normal` | Yes | Default icon **Default**:  `mdi:calendar-blank`
| `icon_today` | Yes | Icon if the anniversary is today **Default**: `mdi:calendar-star`
| `icon_tomorrow` | Yes | Icon if the anniversary is tomorrow **Default**: `mdi:calendar`
---
[<a href="https://www.buymeacoffee.com/V3q9id4" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>](https://www.buymeacoffee.com/V3q9id4)
