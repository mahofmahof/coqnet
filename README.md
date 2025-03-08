# Coqnet Validator Map

This project visualizes Avalanche network validator nodes on a map. It retrieves city and country information from validator IP addresses, color-codes them based on uptime, and lists validators sharing the same location with detailed insights.

## Features
- **Map Visualization**: Validators are displayed using Leaflet on OpenStreetMap.
  - Single validator: Green (uptime ≥ 80%) or Red (uptime < 80%).
  - Multiple validators: Yellow (number of validators shown in popup).
- **Filtering**: Option to show only validators with uptime > 80%.
- **Details**: Popups include city, country, node ID, port, and uptime.
- **Summary**: Country-wise validator counts and a sorted list of validators at the same location.
- **IP Cache**: Locations are cached in `ip_cache.txt` to reduce API calls.

## Usage
1. **Requirements**:
   - Bash, `curl`, and `jq` installed.
   - An Avalanche node running (`127.0.0.1:9650` by default).
   - An [ipinfo.io](https://ipinfo.io) API token (set in `IPINFO_TOKEN` variable).

