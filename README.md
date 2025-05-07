
# Data Analysis and Visualizatio_SIPRI Milexp Dataset (1988-2024)
Data analysis aims to explore the SIPRI dataset on military spending in different regions (continents), and calculate the percentage increase in military spending across different areas from 1988-2024. 

## Code Explanation

### Data Loading and Initial Exploration

The code begins by importing necessary libraries like pandas, NumPy, matplotlib, and seaborn for data manipulation and visualization.
It reads data from a CSV file named 'SIPRI_Milex (3).csv' into a pandas DataFrame called df.
df.head(15) displays the first 15 rows of the DataFrame to provide an initial overview.
print(df.columns) prints the names of all columns in the DataFrame.

### Calculating Percentage Increase

A new column named 'Percentage_Increase_1988_2024' is created to store the percentage increase in military expenditures from 1988 to 2024 for each region. The calculation is done using the formula: ((df['2024'] - df['1988']) / df['1988']) * 100.
A subset of the DataFrame is selected, containing only relevant columns ('Region', '1988', '2024', 'Percentage_Increase_1988_2024'), and stored in df_percentage_increase.
The df_percentage_increase DataFrame is sorted in descending order based on the 'Percentage_Increase_1988_2024' column to show regions with the highest increase first.

### Interactive Bar Chart

The plotly.express library is imported for creating interactive visualizations.
A dictionary is created to store the regional percentage increases in military spending, used as input for the bar chart.
An interactive bar chart is generated using px.bar, displaying the percentage increase for each region with color-coding. The bar chart allows hovering to see precise values.

### Interactive Geo-spatial Map

Similar to the bar chart, data for the geo-spatial map is prepared, including a mapping between regions and their corresponding ISO alpha-3 codes.
px.choropleth is used to create an interactive choropleth map, where regions are colored based on their percentage increase in military spending. The map allows hovering to see region names and percentage increases. Customization options like color scale, projection, and layout are applied to the map.


## Results Explanation

Percentage Increase: The analysis reveals that Asia has experienced the highest percentage increase (374.6%) in military expenditures from 1988 to 2024, followed by Africa (147.3%). Europe shows a minimal increase (3.1%), while North and South America have moderate increases (21.9% and 30.0%, respectively).

Interactive Bar Chart: The bar chart provides a clear visual representation of these percentage increases, with Asia having the tallest bar, followed by Africa, South America, North America, and finally, Europe.

Interactive Geo-spatial Map: The choropleth map visually displays the percentage increases on a world map, coloring regions based on their values. Asia is highlighted with the most intense color due to its high increase, while Europe is colored lightly due to its low increase.

### Language used 
Python
