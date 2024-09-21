

# 🌦️ Historical Weather Forecast

This repository contains a simple Bash script that retrieves and logs real-time weather data for a specific city 🌍 (Jaipur, in this example) using the `wttr.in` service. It processes and extracts observed and forecasted temperatures 🌡️, logging them in a structured format to track daily weather trends 📅.

## ✨ Features

- 📡 Fetches real-time weather data for Jaipur using `curl`.
- 🌡️ Logs observed and forecasted temperatures with timestamps.
- 🗄️ Stores raw weather data for future analysis.

## 📁 Files

- **script.sh**  
  - 📥 Fetches weather data and extracts temperatures.
  - 📝 Logs the data in a structured format.
  
- **weather.log**  
  - 📊 Contains the logged weather data in this format:  
    `year month day hour observed_temp forecasted_temp`
  
- **temperatures.txt**  
  - 📂 Stores the extracted temperature data temporarily.

## 🛠️ How It Works

1. **Fetch Data**:  
   Uses `curl` to retrieve weather data from `wttr.in` for Jaipur 🌍, saving it in a dated file.

2. **Extract Temperatures**:  
   Extracts current and forecasted temperatures 🌡️.

3. **Log Data**:  
   Appends the extracted data with the timestamp 🕒 to `weather.log`.

### 📝 Log Example
```plaintext
year  month  day  hour  observed_temp  forecasted_temp
2024   09     21   04    +30°C         +34°C
```

## 🚀 Usage

### Prerequisites
- Ensure `curl` is installed on your machine 🛠️.
- The script is designed for Linux or macOS systems 💻.

### Running the Script

1. Clone the repository:
   ```bash
   git clone https://github.com/Flack74/Historical-Weather-Forecast/
   cd Historical-Weather-Forecast
   ```

2. Make the script executable:
   ```bash
   chmod +x script.sh
   ```

3. Run the script:
   ```bash
   ./script.sh
   ```

4. Check the `weather.log` for logged weather data:
   ```bash
   cat weather.log
   ```

### 🛠️ Customization
To fetch weather data for a different city, modify the `city` variable in the `script.sh` script:
```bash
city=YourCityName
```

## 🌱 Future Improvements

- 🌍 **Support for Multiple Cities**: Extend the script to log weather data for multiple locations.
- 📊 **Data Visualization**: Create graphical representations of historical weather trends.
- 🚨 **Alerts**: Set up temperature-based notifications for unusual weather patterns.

