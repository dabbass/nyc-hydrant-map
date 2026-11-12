# NYC Fire Hydrant Density Map

An interactive web map showing fire hydrant density across NYC neighborhoods, built with open-source tools and hosted for free on GitHub Pages.

**Technologies:** GDAL/OGR, PostGIS, Python, Docker, Tippecanoe, PMTiles, MapLibre GL JS, GitHub Pages

## About the Project

This project was completed as part of the Modern GIS Accelerator course.

The goal was to take a large spatial dataset, perform some basic analysis, convert the results into a single PMTiles file, and publish an interactive map without paying for hosting or maintaining a map server.

The fire hydrant analysis was mostly a way to explore the technology rather than investigate hydrant distribution in NYC.

## The Process

1. Downloaded NYC open data and prepared it using GDAL/OGR2OGR.
2. Calculated hydrant density by neighborhood using both PostGIS and Python to compare the two approaches.
3. Exported the results to GeoJSON and used Tippecanoe to generate a PMTiles file.
4. Loaded the PMTiles into a MapLibre web map using the course's starter code.
5. Published the map through GitHub Pages.

Docker was used for the PostgreSQL/PostGIS environment.

## What I Learned

The biggest takeaway was how many moving parts there are behind a relatively simple web map.

I spent a fair bit of time troubleshooting PATH issues, Python virtual environments, dependencies, and other configuration problems.

I also got a better understanding of where different technologies fit:

- **PostGIS** is well suited to spatial analysis and data transformations, while **Python** is useful for automating the workflow.
- **PMTiles and vector tiles** make it possible to serve interactive maps without a traditional tile server.
- **GitHub Pages** provides a straightforward way to host a public-facing map for free.
- **GeoServer** and other server-based solutions still have their place, particularly when data access needs to be controlled or server-side services are required.

## What I'd Do Differently

I'd spend more time inspecting the data in QGIS throughout the process. A lot of the initial processing was done through the command line, and without seeing the data, some of the transformations felt pretty abstract.

I'd also pay more attention to the actual analysis results. For this project, I was more interested in getting the technology working than studying NYC's fire hydrant distribution.

For a similar public, read-only web map, I'd definitely consider using this stack again.

## Credits

Built as part of the **Modern GIS Accelerator** course using provided starter code. My focus was on learning the tools, connecting the different parts of the workflow, and getting the application deployed rather than writing the frontend from scratch.