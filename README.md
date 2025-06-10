# Lion Route Optimization

**Lion Route Optimization** is a route optimization tool built with OpenRouteService and Folium to solve multi-vehicle routing problems in Singapore. It calculates and visualizes optimal delivery routes from a home base to multiple customer locations, aiming for minimal travel time and distance.

## Features

* Multi-vehicle route optimization using OpenRouteService
* Interactive map visualization with color-coded routes
* Customizable delivery points and vehicle configurations
* Simple and lightweight Python code, easy to extend

## Use Case

Ideal for logistics companies or services in Singapore needing efficient routing for pickup/delivery tasks, such as:

* Parcel and courier services
* Food or grocery delivery
* Mobile technicians or field agents

## Project Structure

```
Lion_Route_Optimization.ipynb     # Main Jupyter Notebook with implementation
README.md                         # Project description and usage guide
```

## Dependencies

Make sure the following packages are installed:

```bash
pip install openrouteservice folium
```

## Requirements

* Python 3.7+
* A valid [OpenRouteService API key](https://openrouteservice.org/sign-up/)

## How It Works

1. Define delivery points (jobs) and the starting location (home base).
2. Create vehicle objects with capacity and profile (e.g., `driving-car`).
3. Use ORS's optimization endpoint to calculate optimal routes.
4. Decode and visualize routes on a Folium map.
5. Output route details: coordinates, distance, and duration.

## Map Output Example

The result is an interactive map with:

* Markers for each delivery location
* Polyline routes for each vehicle in different colors
* Route details printed below the map

## Usage

Open the notebook in Jupyter or Google Colab and follow the cells sequentially:

```python
# Replace with your OpenRouteService API key
client = ors.Client(key='YOUR_API_KEY')
```

Then run the notebook. The final output will show route details and an interactive map.

## Notes

* Coordinates are in the format `(latitude, longitude)`, but ORS requires `(longitude, latitude)`.
* The code automatically adjusts this.
* Add or remove delivery points by modifying the `coords` list.

## About the Name

“Lion” refers to **Singapura**, known as the “Lion City.” This tool is tailored for urban routing challenges specific to the Singaporean context.

---

