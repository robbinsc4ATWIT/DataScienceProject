# DataScienceProject
# Introduction
The National Basketball Association (NBA) stands as one of the most prestigious professional basketball leagues globally, showcasing top-tier athletes from around the world. As the NBA continues to evolve, teams face the ongoing challenge of effectively evaluating player performance, making informed decisions on player contracts, and predicting player career longevity. In this project, I aim to explore these key aspects of NBA player analysis using a comprehensive dataset encompassing player statistics, contract details, and career trajectories.
# Research Questions
1. Impact of player height on effectivness: This question will explore the physical attribute of height and how it relates to a players key performance metrics. I expect there to be a positive correlation when the NBA is analyzed as a whole.
2. Correlation Increase: I seek to investigate wether there is a correlation between a players increase in contract and their performance.
3. Contract Valuation: Analyzing the relationship between player performance and contract value to determine if certain performance metrics are undervalued or overvalued in player contracts.
# Selection of Data
The model processing and analysis are conducted using Google Collab.

The data contains nearly 500 samples, including most of the NBA players in the league today. For each player there are varied performance metrics and other data points including height, age, wingspan, games played, and player contracts. This is taken from the 2023-2024 which is referred to as 2024 throughout this project, and the 2022-2023 season which is referred to as 2023. This data is pulled from three sources, NBA, ESPN, and Basketball-Reference. Player data was copied to a sheet in excel. Then in other sheets player height data was added and player contract data was added. The player name was used in a VLOOKUP function add new data columns to the player data set. After all the data was on one sheet it was exported to goggle collab for analysis.

Data exceptions: The 2023 contract data did not have all of the players from the 2024 contract data so in some cases the salary and contract increase will be N/A and not included in analysis. Most of these players are rookies for this season or did not play in the previous year, in some cases the data was just not available, but overall there was not much impact on the data set.

A preview of the player data can be seen here:
![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/d39e7db6-6975-42fd-b18b-c2d9e4dd61b2)

In google Collab I further filtered the data using lines of code such as:
![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/62963cd7-99f8-4493-a830-2f7c093241b9)

# methodology
Tools: Pandas, Numpy, Matplotlib.pyplot, seaborn, Excel

My analysis involved data exploration, statistical modeling, and data visualization to address the research questions outlined above. I used various methods such as plotting linear regression coefficients to identify correlation and relationships between variables. For some research questions I put the data into bins to analyze the averages of different groups of data. This helped identify trends throughout the league in a way that is visually legible. I created multiple bar graphs when I plotted the performance metrics, some variables needed a different range and could not all be plotted on the same graph.

In my data exploration phase I would compare many variables and how the related to each other in a seaborn pairplot and heatmap. Through this I was able to identify important statistical information that I could further inspect with other graphs and strategies to answer each research question. I tried many different visualizations and analysis of the data after this initial data exploration which led me to my final graphs where I drew my conclusions. I will include these final graphs in this project report.
