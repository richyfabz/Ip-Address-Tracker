# IP Address Tracker

A modern, responsive web application that allows users to track and visualize the geographical location of any IP address or domain name. Built with React and integrated with IPify's geolocation API and Leaflet maps.

![IP Address Tracker](./screenshot.png)

## Features

- 🌍 **Real-time IP Geolocation** - Track any IP address or domain name
- 🗺️ **Interactive Map** - Visualize locations on an interactive Leaflet map
- 📱 **Fully Responsive** - Works seamlessly on desktop, tablet, and mobile devices
- 🎨 **Modern UI** - Clean and intuitive interface built with Tailwind CSS
- ⚡ **Fast Performance** - Optimized React components for smooth user experience
- 🔍 **Smart Search** - Automatically detects whether input is an IP address or domain

## Demo

Check out the live demo: [Your Demo Link Here]

## Technologies Used

- **React 18.2.0** - Modern JavaScript library for building user interfaces
- **React Leaflet 4.0.1** - React components for Leaflet maps
- **Leaflet 1.8.0** - Leading open-source JavaScript library for mobile-friendly interactive maps
- **Tailwind CSS 3.1.8** - Utility-first CSS framework
- **IPify API** - Geolocation API for IP address tracking
- **Create React App** - Bootstrapped with CRA for easy setup

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher)
- A free API key from [IPify](https://geo.ipify.org/)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ip-address-tracker.git
   cd ip-address-tracker
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   REACT_APP_API_KEY=your_ipify_api_key_here
   ```

   To get your API key:
   - Visit [IPify Geolocation API](https://geo.ipify.org/)
   - Sign up for a free account
   - Copy your API key from the dashboard
   - Paste it in the `.env` file

4. **Start the development server**
   ```bash
   npm start
   ```

   The app will open at [http://localhost:3000](http://localhost:3000)

## Usage

1. **Search by IP Address**
   - Enter any valid IP address (e.g., `8.8.8.8`)
   - Press Enter or click the search button
   - View the location details and map marker

2. **Search by Domain**
   - Enter any domain name (e.g., `google.com`)
   - The app will automatically detect it's a domain
   - View the associated IP address and location

3. **View Location Details**
   - IP Address
   - Location (City, Region)
   - Timezone (UTC offset)
   - Internet Service Provider (ISP)

## Project Structure

```
ip-address-tracker/
├── public/
│   ├── favicon-32x32.png
│   ├── index.html
│   └── manifest.json
├── src/
│   ├── components/
│   │   └── Markerposition.js    # Map marker component
│   ├── images/
│   │   ├── pattern-bg.png       # Header background
│   │   └── icon-arrow.svg       # Search button icon
│   ├── App.js                   # Main application component
│   ├── index.js                 # Application entry point
│   └── index.css                # Global styles
├── .env                         # Environment variables (not in repo)
├── .gitignore
├── package.json
├── tailwind.config.js
└── README.md
```

## Key Components

### App.js
The main component that handles:
- API calls to IPify
- State management for location data
- Form handling and validation
- Rendering the UI and map

### Markerposition.js
A component that:
- Manages the map marker position
- Handles map animations when location changes
- Displays popups with location information

## Build for Production

To create a production build:

```bash
npm run build
```

This creates an optimized build in the `build` folder, ready for deployment.

## Deployment

The app can be deployed to various platforms:

### Netlify
```bash
npm run build
# Drag and drop the 'build' folder to Netlify
```

### Vercel
```bash
npm install -g vercel
vercel
```

### GitHub Pages
```bash
npm install gh-pages --save-dev
# Add to package.json scripts:
# "predeploy": "npm run build",
# "deploy": "gh-pages -d build"
npm run deploy
```

**Important:** Remember to set your `REACT_APP_API_KEY` environment variable in your deployment platform's settings.

## API Rate Limits

The free IPify plan includes:
- 1,000 requests per month
- For higher limits, check [IPify pricing](https://geo.ipify.org/pricing)

## Troubleshooting

### Map not displaying
- Ensure `leaflet/dist/leaflet.css` is imported in App.js
- Check that Leaflet marker icons are properly configured

### API errors
- Verify your API key is correctly set in `.env`
- Ensure you've restarted the dev server after creating/modifying `.env`
- Check that you haven't exceeded your API rate limit

### Blank page after compilation
- Check browser console for JavaScript errors
- Verify all image assets are in the correct directory
- Ensure the Markerposition component is properly created

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Challenge by [Frontend Mentor](https://www.frontendmentor.io)
- Geolocation data provided by [IPify](https://www.ipify.org/)
- Map tiles by [OpenStreetMap](https://www.openstreetmap.org/)
- Icons and design assets from Frontend Mentor

## Contact

Your Name - [@yourtwitter](https://twitter.com/yourtwitter)

Project Link: [https://github.com/yourusername/ip-address-tracker](https://github.com/yourusername/ip-address-tracker)

---

⭐ If you found this project helpful, please give it a star!