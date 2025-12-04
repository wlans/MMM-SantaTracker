# MMM-SantaTracker
This is a module for the [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror) framework that will track Santa Claus as he delivers presents on Christmas Eve.

![MMM-SantaTracker interface](ScreenShot.PNG)

## Features
* Tracks Santa Claus as he delivers presents!
* Displays popup of his location with city & country 
* Displays photo of the location where he's dropping off gifts or coal
* Three map options


## Installation
Clone the repository and add the config settings.
1. Clone the repository into your `~/MagicMirror/modules` folder.
2. Configure your `~/MagicMirror/config/config.js` file.
```
{
	module: "MMM-SantaTracker",
	position: "bottom_left",
	config: {
		markerColor: 'IndianRed',
		mapMode: "satellite"
	}
},
``````

## Options
All configuration parameters are optional.
| Option | Default | Description |
|:------:| ------- | ----------- |
| markerColor | "LightGreen" | Color of the points marking the cities |
| mapMode | "dark" | The map tile style. Accepted parameters are "dark", "light", "satellite"|
| lineColor | "#a1100" | Color of the line that follows Santa |
| lineWidth | 3 | Width of the line that follows Santa |
| overTime | null | **Testing Mode**: Overrides the current time to simulate Santa's journey on Christmas Eve. When set to a date/time string (format: `YYYY-MM-DDTHH:mm:ss.sssZ`), the module will start tracking from that point and automatically advance time by 1 minute with each update interval. This allows you to test the tracker any time of year by setting a Christmas Eve date/time (e.g., `"2025-12-24T18:00:00.000Z"`). The tracker will progress through Santa's route as if time is passing. Leave as `null` for normal real-time operation on Christmas Eve. |
| debug | false | Enable debug logging. Set to `true` to see detailed console logs about Santa's location updates, map building, and data processing. Useful for troubleshooting. |

