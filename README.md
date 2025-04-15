# Delivery Service Coverage Map Generator

## Overview
This project generates and visualizes delivery service coverage areas using multiple APIs including Shipday, OpenRoute, and Google Maps. It helps identify valid delivery zones by testing multiple points and adjusting their locations based on service availability.

## Features
- Generates points in a circular pattern around a central location
- Validates delivery service availability using Shipday API
- Calculates driving distances using OpenRoute Services
- Geocodes addresses using Google Maps API
- Creates interactive maps using Folium
- Exports data to CSV and HTML formats

## Prerequisites
- Python 3.8+
- Required API keys:
  - Shipday API key
  - OpenRoute Services API key 
  - Google Maps API key

## Installation

1. Clone the repository:
```sh
git clone https://github.com/yourusername/delivery-coverage-map.git
cd delivery-coverage-map
```

2. Install required packages:
```sh
pip install -r requirements.txt
```

3. Set up environment variables:
   - Copy .env.example to `.env`
   - Add your API keys to the `.env` file:
```sh
SHIPDAY_API_KEY=your_shipday_key_here
OPENROUTE_API_KEY=your_openroute_key_here
GOOGLE_MAPS_API_KEY=your_google_maps_key_here
```

## Usage
1. Open `Mapping Project Jupyter_Final.ipynb` in Jupyter Notebook
2. Update the starting point coordinates if needed:
```python
start_lat, start_lon = 32.0646381, -81.2050952

Also change on Pickup address for the formatted address:
# Map pickup address
pickup_address='1450 Dean Forest Road, Garden City, GA 31405-9365, USA' # Use this line to manually set the address
```
3. Run all cells to generate the coverage map

## Project Structure
```
delivery-coverage-map/
├── .env                     # API keys configuration
├── .env.example            # Example environment file
├── requirements.txt        # Python dependencies
├── Mapping Project Jupyter_Final.ipynb  # Main notebook
└── data/                   # Generated data directory
    ├── JSONs/             # API response data
    ├── Maps_data/         # CSV exports
    └── Maps_HTML/         # Generated maps
```

## Setting Up Git Repository

1. Initialize git repository:
```sh
git init
```

2. Create `.gitignore` file:
```
# Environment variables
.env

# Generated data
data/
.ipynb_checkpoints/
__pycache__/
```

3. Add and commit files:
```sh
git add .gitignore README.md requirements.txt "Mapping Project Jupyter_Final.ipynb"
git commit -m "Initial commit"
```

4. Link to GitHub:
```sh
git branch -M main
git remote add origin https://github.com/yourusername/delivery-coverage-map.git
git push -u origin main
```

## Security Notes
- Never commit `.env` file containing API keys
- Keep .env.example as a template
- Document required API keys in README.md

## License
MIT License

## Contributing
1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## Contact
For questions or support, please open an issue in the GitHub repository.