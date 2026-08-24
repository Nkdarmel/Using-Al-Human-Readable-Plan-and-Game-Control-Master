# Weather Dashboard

A beautiful, responsive weather dashboard that displays real-time weather information from multiple cities using the OpenWeatherMap API.

## Features

✨ **Key Features:**
- 🌍 Search weather by city name
- 🌡️ Display current temperature, humidity, wind speed, and pressure
- 🎨 Beautiful gradient UI with smooth animations
- 📱 Fully responsive design for mobile and desktop
- 🔄 Real-time weather updates
- ⭐ Quick access to popular cities
- 🎯 Multiple weather cards for comparing cities
- ❌ Remove individual weather cards
- 🌙 Weather icons for visual clarity

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- OpenWeatherMap API key (optional for demo mode)

### Installation

1. Clone or download the project files
2. Open `index.html` in your web browser
3. Start searching for cities!

## Usage

### Basic Features

1. **Search for a City:**
   - Type the city name in the search box
   - Click "Search" or press Enter
   - Weather data will be displayed in a card

2. **Quick City Access:**
   - Click any city button in the "Popular Cities" section
   - Pre-configured with: London, New York, Tokyo, Sydney, Dubai, Paris

3. **Manage Weather Cards:**
   - Click the ✕ button on any card to remove it
   - Compare multiple cities by searching for several

### API Integration

To use real weather data, follow these steps:

1. **Get an API Key:**
   - Visit [OpenWeatherMap](https://openweathermap.org/api)
   - Sign up for a free account
   - Create an API key from your dashboard

2. **Configure the App:**
   - Open `app.js`
   - Replace `const API_KEY = 'demo'` with your actual API key
   - Uncomment the real API fetch code (see comments in app.js)

## Display Information

Each weather card shows:
- City name and country code
- Current temperature and "feels like" temperature
- Weather description with icon
- Humidity percentage
- Wind speed (m/s)
- Atmospheric pressure (hPa)
- Cloud coverage percentage

## Customization

### Add Default Cities
Edit the `defaultCities` array in `app.js`:
```javascript
const defaultCities = ['London', 'New York', 'Tokyo', 'Your City'];
```

### Modify Colors
Edit the CSS gradient in `styles.css`:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Change Update Interval
Modify the timeout values in `app.js` to refresh weather data automatically.

## Weather Icons

The dashboard uses emoji icons for visual representation:
- ☀️ Clear sky (day)
- 🌙 Clear sky (night)
- ⛅ Few clouds
- ☁️ Overcast
- 🌧️ Rain
- ⛈️ Thunderstorm
- ❄️ Snow
- 🌫️ Mist/Fog

## Technologies Used

- **HTML5** - Structure and semantics
- **CSS3** - Styling with animations and gradients
- **JavaScript (ES6+)** - Dynamic functionality
- **OpenWeatherMap API** - Real weather data (optional)

## File Structure

```
weather-dashboard/
├── index.html      # HTML structure
├── styles.css      # Styling and animations
├── app.js          # JavaScript logic
└── README.md       # This file
```

## API Response Format

The app expects weather data in the following format:
```json
{
  "name": "London",
  "sys": { "country": "GB" },
  "main": {
    "temp": 15,
    "feels_like": 14,
    "humidity": 72,
    "pressure": 1013
  },
  "weather": [{
    "main": "Clouds",
    "description": "overcast clouds",
    "icon": "04d"
  }],
  "wind": { "speed": 4.5 },
  "clouds": { "all": 90 }
}
```

## Error Handling

- ❌ Shows error messages for failed API requests
- ⚠️ Handles invalid city names gracefully
- 🔄 Implements retry logic for network issues

## Performance Optimizations

- Lazy loading of weather data
- Smooth CSS animations with hardware acceleration
- Debounced search inputs
- Optimized DOM manipulation
- Local caching of weather data

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Future Enhancements

- [ ] Hourly forecast view
- [ ] 5-day forecast
- [ ] Weather alerts
- [ ] Location-based auto-detection
- [ ] Dark/Light theme toggle
- [ ] Favorite cities storage
- [ ] Historical weather data
- [ ] Weather maps integration

## Troubleshooting

### "Weather data not found"
- Check spelling of the city name
- Try using the city code (e.g., "LON" for London)
- API might have rate limits - wait a moment before searching

### Cards not appearing
- Check browser console for errors (F12)
- Verify API key is valid (if using real API)
- Clear browser cache and reload

### Slow performance
- Reduce the number of active weather cards
- Check internet connection speed
- Close other browser tabs

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues or questions, please create an issue in the repository or contact the maintainer.

---

**Enjoy tracking weather in your favorite cities! 🌍**
