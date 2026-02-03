# Environmental Monitoring & Alert System

A comprehensive web-based environmental monitoring system that provides real-time data on air quality, weather conditions, and environmental risk assessment.

## Features

✅ **Real-time Environmental Data**
- Temperature and humidity monitoring
- Wind speed and direction
- Atmospheric pressure
- Visibility metrics
- UV index

✅ **Air Quality Monitoring**
- Air Quality Index (AQI)
- PM2.5 and PM10 particulate matter
- Ozone (O₃) levels
- Nitrogen Dioxide (NO₂) levels

✅ **Intelligent Risk Assessment**
- Multi-factor environmental risk scoring
- Correlation analysis between environmental factors
- Contextual alerts for high-risk conditions
- Pattern detection (e.g., high PM2.5 + low wind = pollution accumulation)

✅ **Data Visualization**
- Interactive map with location markers
- 24-hour temperature and humidity trend charts
- Real-time data updates
- Responsive design for all devices

✅ **User-Friendly Interface**
- Search by city name or coordinates
- Automatic geolocation support
- Clean, modern dark theme
- Intuitive dashboard layout

## Quick Start

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- Modern web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Sreemsun/Environment-monitoring-and-alert-system.git
   cd Environment-monitoring-and-alert-system
   ```

2. **Install dependencies**
   ```bash
   pip install -r backend/requirements.txt
   ```

3. **Configure API Keys**
   - Copy `.env.example` to `.env`
   - Add your API keys to the `.env` file
   - Sign up at [weatherapi.com](https://www.weatherapi.com/) for Weather API key

4. **Run the application**
   ```bash
   python run.py
   ```
   Or on Windows:
   ```powershell
   .\backend\start_server.ps1
   ```

5. **Access the application**
   - Open your browser and go to `http://localhost:5000`
   - The static files will be served automatically

## How to Use

1. **Search for a Location**
   - Enter a city name (e.g., "London", "New York", "Tokyo")
   - Or enter coordinates (e.g., "51.5074,-0.1278")
   - Click "Monitor Location" or press Enter

2. **Use Current Location**
   - Click the location button (📍) to automatically detect your location
   - Grant location permission when prompted

3. **View Environmental Data**
   - Current conditions (temperature, humidity, wind, etc.)
   - Air quality index and pollutant levels
   - Environmental risk score
   - Correlation analysis
   - Historical trends chart
   - Interactive map

## API Configuration

The system uses the following APIs:

### WeatherAPI.com (Primary Data Source)
- **Free Tier**: 1,000,000 calls/month
- Provides: Weather data, forecasts, and air quality
- Get your free API key at [weatherapi.com](https://www.weatherapi.com/)

### OpenAI (Optional - AI-powered insights)
- Get your API key at [platform.openai.com](https://platform.openai.com/)
- Add to `.env` file for AI-powered environmental insights

## Technical Stack

- **Backend**: Python Flask
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Database**: SQLite (for historical data)
- **Mapping**: Leaflet.js
- **Charts**: Chart.js
- **APIs**: WeatherAPI.com, OpenAQ, OpenAI
- **Icons**: Font Awesome

## Features Breakdown

### Risk Scoring Algorithm
The system calculates environmental risk based on:
- Temperature extremes (>35°C or <-10°C)
- Humidity levels (<20% or >80%)
- Wind speed (>50 km/h)
- Air quality (EPA Index)
- UV index (>8)

Risk levels:
- **Low Risk**: 0-30
- **Moderate Risk**: 31-60
- **High Risk**: 61-100

### Correlation Analysis
The system detects:
- High PM2.5 + Low wind = Poor air dispersion
- High temperature + High PM2.5 = Ozone formation risk
- High humidity + High temperature = Heat stress
- High UV + Clear skies = Sun protection needed
- Low pressure = Weather changes likely

### Auto-Refresh
- Data automatically refreshes every 5 minutes
- Real-time clock updates every second
- Manual refresh available via search

## Browser Compatibility

✅ Chrome/Edge (recommended)
✅ Firefox
✅ Safari
✅ Opera

Requires JavaScript enabled and internet connection.

## Project Structure

```
Environment-monitoring-and-alert-system/
├── backend/                    # Backend Flask application
│   ├── app.py                 # Main Flask application
│   ├── database.py            # Database operations
│   ├── predictions.py         # ML predictions
│   ├── requirements.txt       # Python dependencies
│   └── start_server.ps1       # Windows startup script
├── static/                    # Frontend static files
│   ├── index.html            # Main page
│   ├── dashboard.html        # Dashboard page
│   ├── style.css             # Styles
│   ├── script.js             # Frontend JavaScript
│   └── test_historical.html  # Historical data test page
├── docs/                      # Documentation
│   ├── AI_SETUP_GUIDE.md
│   ├── BACKEND_GUIDE.txt
│   ├── HISTORICAL_GRAPH_GUIDE.md
│   ├── HISTORICAL_SYSTEM_GUIDE.md
│   ├── SENSOR_MAP_GUIDE.md
│   ├── BACKEND_FEATURES.txt
│   └── SETUP_GUIDE.txt
├── .gitignore                # Git ignore rules
├── .env.example              # Environment variables template
├── run.py                    # Application launcher
└── README.md                 # This file
```

## Future Enhancements

Potential additions:
- ✅ Historical data storage (SQLite database implemented)
- ✅ AI-powered environmental insights
- ✅ Predictive analytics using machine learning
- Comparison between multiple locations
- Email/SMS alerts for critical conditions
- More data sources (OpenAQ, PurpleAir)
- Export data to CSV/PDF
- Weather radar overlay
- Air quality forecast

## Deployment

### Local Development
```bash
python run.py
```

### Production Deployment Options

1. **Heroku**
   ```bash
   # Create Procfile
   echo "web: python run.py" > Procfile
   
   # Deploy
   heroku create your-app-name
   git push heroku main
   ```

2. **Docker**
   ```dockerfile
   # Create Dockerfile
   FROM python:3.9
   WORKDIR /app
   COPY . .
   RUN pip install -r backend/requirements.txt
   CMD ["python", "run.py"]
   ```

3. **AWS/GCP/Azure**
   - Use the provided `run.py` as entry point
   - Set environment variables from `.env`
   - Configure port binding

## Troubleshooting

**Problem**: Location not found
- **Solution**: Check spelling, try coordinates instead

**Problem**: No data displayed
- **Solution**: Check internet connection, try a different location

**Problem**: Geolocation not working
- **Solution**: Grant location permission in browser settings

**Problem**: Map not loading
- **Solution**: Check internet connection, refresh page

## License

This project is open source and available for educational and personal use.

## Credits

- Weather data: [WeatherAPI.com](https://www.weatherapi.com/)
- Maps: [OpenStreetMap](https://www.openstreetmap.org/) & [Leaflet.js](https://leafletjs.com/)
- Charts: [Chart.js](https://www.chartjs.org/)
- Icons: [Font Awesome](https://fontawesome.com/)

## Contact & Support

For issues, suggestions, or contributions, please contact the development team.

---

**Built with ❤️ for environmental awareness**

Last Updated: January 2026
