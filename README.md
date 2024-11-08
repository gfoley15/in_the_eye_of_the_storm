# in_the_eye_of_the_storm

## About
This project was inspired by my desire to understand the impact of hurricanes, particularly on the Gulf Coast of Southwest Florida. As a Minnesotan, hurricanes were once a distant concern, but frequent vacations to Florida sparked an interest in these powerful weather phenomena. The project aims to:

1. Educate about the nature and impact of hurricanes
2. Analyze historical hurricane data to identify trends and patterns
3. Provide a resource for staying informed about potential storms
4. Showcase technical skills in data analysis and visualization

Special thanks to Ryan Hall Y'all, Mike's Weather Page, and Tropical Tidbits for their inspirational weather insights and hurricane coverage.
- https://www.youtube.com/@RyanHallYall
- https://www.facebook.com/mikesweatherpage/
- https://www.tropicaltidbits.com/

## Technologies Used
- Web Scraping: BeautifulSoup
- Data Processing: Python, Pandas, Polars
- Development Environment: Jupyter Notebook
- Database: MongoDB
- Visualization: Power BI

## Data Sources
Data was sourced from the National Oceanic and Atmospheric Administration (NOAA), focusing on:

1. Most intense US hurricane landfalls
2. Best track data provided by the Hurricane Hunters Air Force Unit

This data includes crucial metrics such as location, pressure, wind speed, wind gusts, wind direction, storm speed, and storm direction.

Data has been published on Kaggle: https://www.kaggle.com/datasets/garrettfoley/major-north-atlantic-hurricanes/data

## Project Workflow
### 1. Extract
- Web scraped NOAA hurricane data for most intense US Landfalls
- Exported track data to CSV format

### 2. Transform
Hurricane Dataframe Cleaning:
- Removed unnecessary fields and unnamed storms
- Cleaned date/time fields
- Converted latitude and longitude
- Standardized numeric columns
- Sorted by date

Track Data Processing:
- Focused on USA regional data
- Analyzed hurricane frequency and data points
- Sorted chronologically

Created a key-value pair relationship for affected states to enhance Power BI modeling.

### 3. Load
- Created a MongoDB database with two collections for each dataset
- Prepared data for further analysis and direct Power BI connection

### 4. Visualize
Developed a Power BI model and dashboard to visualize:
- Hurricane data and track information
- Analysis of Florida hurricane landfalls
- Pressure and wind speed trends

## Challenges and Solutions
1. **Data Source Changes**: NOAA website URL changed mid-project. Solution: Leveraged previously collected data to continue analysis.
2. **Firewall Issues**: MongoDB code execution and Power BI connection were blocked. Solution: Utilized CSV Power BI connection as an alternative.
3. **Complex Data Relationships**: Difficulty in managing states affected by storms. Solution: Implemented data splitting and merging techniques to create a simplified table structure.
4. **Data Volume Management**: Track data was initially over-inclusive. Solution: Refined data selection process to focus on relevant storm data points, particularly for reused storm names.

## Future Improvements
- Gather new seasonal hurricane data
- Expand analysis to include storm surge/inundation, global ocean temperature and financial impact of storm damages
- Create an interactive web page and API for public use
