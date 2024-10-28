# Exoplanet Habitability Analysis
## URL of the streamlit app
`https://project02-jusu88p4kffe54xc8kzvdg.streamlit.app/`
## Overview
This Streamlit app explores the habitability of exoplanets by analyzing various criteria that might indicate a planet's potential to support life. The application pulls data from the NASA Exoplanet Archive and applies filters based on size, orbital period, and host star characteristics to highlight planets that could be habitable. 

## Features
- **Data Fetching**: The app retrieves the latest exoplanet data from the NASA Exoplanet Archive via `astroquery`.
- **Data Cleaning**: Rows with missing values in essential columns are removed to ensure accuracy.
- **Habitability Criteria**: A custom function flags planets as "potentially habitable" based on distance from the host star (using stellar flux) and planet characteristics (radius and mass).
- **Interactive Visualization**: Users can visualize the relationship between star temperature and distance from the host star in a logarithmic scatter plot, with hover details for each planet.

## Code Structure
The main elements of the Streamlit code are as follows:

1. **Data Retrieval**: 
   - The app uses `astroquery` to pull data from the NASA Exoplanet Archive. This includes various parameters such as orbital period, radius, mass, and host star characteristics.

2. **Data Cleaning**:
   - The data is cleaned by dropping rows with missing values in critical columns like `pl_orbper` (orbital period), `pl_rade` (planet radius), `pl_masse` (planet mass), and `st_teff` (star temperature).

3. **Habitability Filter**:
   - A function calculates stellar flux limits to define a habitable zone around the star, filtering planets that fall within this zone and have a suitable radius and mass.

4. **Visualization**:
   - The app uses Plotly to create an interactive scatter plot of star temperature against distance from the star (AU), with a logarithmic x-axis. Hover functionality allows the user to view planet names and other details.

## Getting Started

### Prerequisites
- **Python** (version 3.7 or higher)
- Install the required packages using:
  ```bash
  pip install streamlit astroquery plotly pandas matplotlib
  ```

### Running the App
1. Clone this repository.
2. In the project directory, run:
   ```bash
   streamlit run app.py
   ```
3. Open the provided local URL in a web browser to view the app.

### File Descriptions
- `app.py`: The main Streamlit app script.
- `README.md`: Documentation for understanding the code and usage.
- `exoplanet_data_extended.csv` and `cleaned_exoplanet_data.csv`: Files created during the data retrieval and cleaning process.

## Future Improvements
- **Enhanced Interaction**: Adding click functionality to display detailed planet data.
- **Additional Filters**: Allow users to filter based on additional planetary or stellar attributes.


