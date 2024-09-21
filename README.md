# Historical Weather Forecast

This repository contains a simple script that retrieves and logs weather data for a specific city (Jaipur, in this example) using the wttr.in service. The script processes raw data to extract the observed and forecasted temperatures, then logs these in a structured format. The result is a daily log file that records weather trends over time.

## Features

- Fetches real-time weather data for Jaipur using `curl`.
- Extracts observed and forecasted temperatures in Celsius.
- Logs temperatures along with the timestamp in a structured format (`rx_poc.log`).
- Stores the raw weather data for further analysis or archiving.
  
## Files

- **rx_poc.sh**  
  The core script that:
  1. Fetches the current weather report from wttr.in.
  2. Extracts temperature information and timestamps.
  3. Appends the data to the log in a structured format.
  
- **rx_poc.log**  
  This log file stores the daily weather data in the following format:
  ```
  year   month   day   hour   observed_temperature   forecasted_temperature
  ```

- **temperatures.txt**  
  Temporary file to store temperature data extracted from the raw weather report.

## How It Works

1. **Fetching the Data**  
   The script uses `curl` to fetch the current weather report from wttr.in for Jaipur. The data is stored in a file named with the current date, `raw_data_YYMMDD`.

2. **Temperature Extraction**  
   The script processes the raw weather data to extract:
   - **Observed Temperature**: The current temperature at the time of the request.
   - **Forecasted Temperature**: The expected temperature based on the forecast for the near future.

3. **Data Logging**  
   The extracted temperatures, along with the current timestamp (year, month, day, hour), are appended to `rx_poc.log`.

### Log Example
```plaintext
year    month   day   hour   obs_tmp    fc_temp
2024    09      21    04     +30°C      +34°C
```

## Usage

### Prerequisites
- Ensure you have `curl` installed on your machine.
- The script assumes you're running on a Linux or macOS system.

### Running the Script

1. Clone the repository:
   ```bash
   git clone https://github.com/Flack74/Historical-Weather-Forecast/
   cd Historical-Weather-Forecast
   ```

2. Make the script executable:
   ```bash
   chmod +x rx_poc.sh
   ```

3. Run the script:
   ```bash
   ./rx_poc.sh
   ```

4. Check the `rx_poc.log` for logged weather data:
   ```bash
   cat rx_poc.log
   ```

### Customization
To fetch weather data for a different city, modify the `city` variable in the `rx_poc.sh` script:
```bash
city=YourCityName
```

## Future Improvements

- **Support for Multiple Cities**: Extend the script to log weather data for multiple cities.
- **Data Visualization**: Use the logged data to create graphical representations of historical weather trends.
- **Alerts**: Set up temperature-based alerts to notify users of unusual weather patterns.


---
