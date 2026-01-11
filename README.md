# Weather Dashboard - TRMNL Plugin

A beautiful weather dashboard plugin for TRMNL that displays current conditions and a 3-day forecast with dot-matrix style numbers and weather icons.

![Weather Dashboard Preview](https://img.shields.io/badge/TRMNL-Plugin-blue)

## Features

- **Current Weather Display**: Large dot-matrix style temperature display with current conditions
- **High/Low Temperatures**: Today's temperature range with up/down arrows
- **Visual Weather Icons**: 8 different weather condition indicators (sunny, cloudy, rain, snow, fog, etc.)
- **3-Day Forecast**: Compact forecast view with temperatures and weather icons
- **Dark/Light Mode**: Toggle between dark and light color schemes
- **Location Display**: Shows your location name and coordinates
- **Last Update Time**: Displays when the weather data was last refreshed
- **Customizable Units**: Choose between Celsius and Fahrenheit

## Screenshots

The plugin features a modern, minimalist design optimized for e-ink displays:

- **Left Panel**: Large current temperature with dot-matrix rendering, weather condition icons, and location info
- **Right Panel**: 3-day forecast with day names, high/low temperatures, and weather icons

## Installation

1. Copy all plugin files to your TRMNL plugins directory
2. Configure the plugin settings in the TRMNL dashboard
3. Add the plugin to your desired layout

## Configuration

### Required Settings

- **Location**: A friendly name for your location (e.g., "Home", "New York")
- **Latitude**: Your location's latitude coordinate
- **Longitude**: Your location's longitude coordinate

> **Tip**: Use [GPS Coordinates](https://www.gps-coordinates.net/) to find your exact latitude and longitude.

### Optional Settings

- **Temperature Unit**: Choose between Celsius (°C) or Fahrenheit (°F)
  - Default: Celsius
- **Color Mode**: Select Dark or Light theme
  - Default: Dark

## Data Source

This plugin uses the [Open-Meteo API](https://open-meteo.com/) to fetch weather data:

- Current temperature and weather conditions
- Daily high/low temperatures
- 4-day forecast data
- Automatic timezone handling

**Refresh Interval**: 60 minutes

## Weather Codes

The plugin supports all WMO Weather Interpretation Codes:

| Icon | Conditions |
|------|------------|
| ☀️ Sunny | Clear sky (codes 0, 1) |
| ☁️ Cloudy | Partly cloudy, overcast (codes 2, 3) |
| 🌧️ Rain | Drizzle, rain, rain showers (codes 51-67, 80-82) |
| ❄️ Snow | Snow, snow showers (codes 71-75, 85-86) |
| 🌫️ Foggy | Fog, depositing rime fog (codes 45, 48) |
| ❄️ Snow Grains | Snow grains (code 77) |
| 💨 Strong Wind | Thunderstorm (code 95) |
| ⚡ Lightning | Thunderstorm with hail (codes 96, 99) |

## Supported Layouts

- ✅ Full (800x480)
- ✅ Half Horizontal
- ✅ Half Vertical
- ✅ Quadrant

## Technical Details

### Dot-Matrix Rendering

The plugin uses a custom JavaScript rendering system to display numbers in a retro dot-matrix style:

- 5×7 grid for each character
- Supports digits 0-9, letters a-z, and special symbols (°, -, ↑, ↓)
- Rounded rectangles for a modern aesthetic
- Dynamic sizing for different display contexts

### Files

- `shared.liquid`: Core logic, styles, and rendering functions
- `full.liquid`: Full-screen layout template
- `half_horizontal.liquid`: Half-width horizontal layout
- `half_vertical.liquid`: Half-height vertical layout
- `quadrant.liquid`: Quarter-screen layout
- `settings.yml`: Plugin configuration and metadata

## Customization

### Color Modes

**Dark Mode** (default):
- Background: Black (#000000)
- Active pixels: White (#FFFFFF)
- Inactive pixels: Dark gray (#232323)

**Light Mode**:
- Background: Light gray (#D9D9D9)
- Active pixels: Black (#000000)
- Inactive pixels: Light gray (#D9D9D9)

### Typography

The plugin uses **Roboto Mono** for a clean, modern monospace aesthetic that complements the dot-matrix number rendering.

## Credits

**Author**: trmnl@achtnegen.nl

**Updates**:
- v1.1: Updated the 3 and 8 digit rendering (thanks Maximillian!)
- v1.0: Initial release

**Powered by**: [Open-Meteo API](https://open-meteo.com/)

**Weather Icons**: [Weather Icons](https://github.com/erikflowers/weather-icons) by Erik Flowers

## License

This plugin is provided as-is for use with TRMNL devices.

## Support

For issues, questions, or feature requests, please contact: trmnl@achtnegen.nl

---

Made with ❤️ for TRMNL
