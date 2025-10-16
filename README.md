# TRACETN – Trentino Analysis of Commuter Exchanges

**TRACETN** is a data-driven project that analyses and visualizes the commuting flows between municipalities in the Trentino region (Italy).  
It combines open mobility data, population statistics, and network models to explore the *invisible roads* that connect people’s daily lives.

---

## Objectives
- Build an **Origin–Destination matrix** of commuter flows across Trentino.
- Model **inbound and outbound** commuting using official data sources.
- Integrate **distance and travel-time matrices** computed with GraphHopper.
- Provide **indicators per capita** to study local labor accessibility and dependencies.
- Visualize the network of movements as a **mobility graph**.

---

## Data Sources
- Provincial commuter datasets (entrances and exits by municipality)
- Population dataset (average 2021 residents per municipality)
- Distance and travel-time matrix generated with a local **GraphHopper** instance
- Geographic coordinates retrieved from **OpenStreetMap / Nominatim**

---

## Methods
1. **Data Cleaning & Integration**  
   Harmonization of municipality codes and merging of inbound/outbound flows.
2. **Geocoding & Routing**  
   Using Nominatim for coordinates and GraphHopper (car profile) for realistic road distances.
3. **Network Modeling**  
   Building a directed weighted graph (`networkx`) where nodes are municipalities and edges represent commuter intensity.
4. **Indicators**  
   - Net commuting balance  
   - Commuters per capita  
   - Commuting accessibility index  
   - Cross-municipality dependency ratio

---

## Visualizations
- Choropleth maps of **net commuting balance**
- Network graphs showing **dominant commuting flows**
- Interactive dashboards (in development)
