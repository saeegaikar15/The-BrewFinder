# BrewFinder

BrewFinder is a responsive, single-page coffee-shop finder. Search by city, neighborhood, or postal code, or use browser location to see nearby cafés on an interactive map.

## Run it

Open `BrewFinder.html` in a modern browser. For best results—especially with browser location permissions—serve the `outputs` folder over localhost instead of opening the file directly. For example, from that folder run:

```powershell
python -m http.server 8000
```

Then visit <http://localhost:8000/BrewFinder.html>.

## Features

- Location search and browser geolocation
- Café cards with distance, mapped position, address, and available tags
- Filters for open status, Wi-Fi, top ratings, and drive-through
- Sorting by distance or rating, plus Google Maps directions
- Responsive layout for desktop and mobile
- Initial San Francisco demo cafés for a quick preview

## Data and services

Searches geocode locations with OpenStreetMap Nominatim and request nearby cafés from public Overpass API instances. Map tiles use OpenStreetMap.de. These public services require an internet connection and may be slow or unavailable. Ratings, opening hours, and amenities are shown only when available; OpenStreetMap café records often do not include them. Initial demo cards are illustrative and are replaced when a search is made.

The page also loads Leaflet, fonts, and café imagery from external CDNs. No API key is embedded. For a production deployment, review each provider's usage policy and consider using a managed backend or commercial place-data service for reliable search and business details.

## Geolocation troubleshooting

If **Use My Location** times out or is denied, allow location access in the browser and check that device location services are enabled. Searching by city or postal code is an alternative. Serving the page from `localhost` can also help with browser permission handling.
