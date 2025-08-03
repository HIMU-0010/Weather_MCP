# Weather MCP Server

A Model Context Protocol (MCP) server that provides weather data using the Open-Meteo API. This server allows AI assistants to retrieve current weather conditions and forecasts for any location on Earth.

## Features

- **Current Weather**: Get real-time temperature, wind speed, humidity, and weather conditions
- **Weather Forecast**: Retrieve hourly forecasts for up to 7 days
- **Weather Summary**: Get a comprehensive summary including current conditions and daily min/max temperatures
- **Global Coverage**: Works with any latitude/longitude coordinates worldwide
- **No API Key Required**: Uses the free Open-Meteo API

## Installation

1. Clone or download this repository

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   npm start
   ```
### Available Tools

The server provides three main tools:

#### 1. `get_current_weather`
Get current weather data for a specific location.

**Parameters:**
- `latitude` (number): Latitude of the location
- `longitude` (number): Longitude of the location

**Example:**
```json
{
  "name": "get_current_weather",
  "arguments": {
    "latitude": 52.52,
    "longitude": 13.41
  }
}
```

#### 2. `get_weather_forecast`
Get hourly weather forecast for a specific location.

**Parameters:**
- `latitude` (number): Latitude of the location
- `longitude` (number): Longitude of the location
- `days` (number, optional): Number of days to forecast (default: 7)

**Example:**
```json
{
  "name": "get_weather_forecast",
  "arguments": {
    "latitude": 52.52,
    "longitude": 13.41,
    "days": 3
  }
}
```

#### 3. `get_weather_summary`
Get a summary of current weather and today's forecast for a location.

**Parameters:**
- `latitude` (number): Latitude of the location
- `longitude` (number): Longitude of the location

**Example:**
```json
{
  "name": "get_weather_summary",
  "arguments": {
    "latitude": 52.52,
    "longitude": 13.41
  }
}
```

## API Reference

This server uses the [Open-Meteo API](https://open-meteo.com/)


## Happy coding! 🚀
