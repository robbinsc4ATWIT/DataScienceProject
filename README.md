# DataScienceProject
# Introduction
The National Basketball Association (NBA) stands as one of the most prestigious professional basketball leagues globally, showcasing top-tier athletes from around the world. As the NBA continues to evolve, teams face the ongoing challenge of effectively evaluating player performance, making informed decisions on player contracts, and predicting player career longevity. In this project, I aim to explore these key aspects of NBA player analysis using a comprehensive dataset encompassing player statistics, contract details, and career trajectories.
# Research Questions
1. Impact of player height on effectivness: This question will explore the physical attribute of height and how it relates to a players key performance metrics. I expect there to be a positive correlation when the NBA is analyzed as a whole.
2. If a players contract increases does their performance increase as well: I seek to investigate wether there is a correlation between a players increase in contract and their performance.
3. Performance metrics as it relates to contract valuations: Analyzing the relationship between player performance and contract value to determine if certain performance metrics are undervalued or overvalued in player contracts.
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

# Results

Impact of player height on effectivness:

![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/588a936d-1012-47ca-9a9b-da6b082a4d4f)

![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/4f1efd20-6d53-4b36-b1a7-089a620ae88a)

The overall conclusion is that height does not impact a players effectiveness on the court. There is some positive correlation between Rebounds, FG%, and Blocks per game, but in other key areas such as points, assists, or plus minus, there is little or negative correlation. Rebounds and blocks are a defensive attribute and it is obvious that the taller a person is the easier it is to get to a ball in the air which explains the positive correlation in these metrics. Field goal percentage is a less obvious metric to be somewhat correlated to height. This is explained by the shot selection of taller players. Many tall players in the league are finishing from right under the hoop or inside the paint, there is less margin for error the closer you get to the basket. The other important stats that make up effective players have no correlation to height, therefore, with the reasons explaining the somewhat correlated stats, I can assume that height does not impact a players effectiveness.




If a players contract increases does their performance increase as well:

For this question I decided to graph certain performance metrics by position where the players increase in contract was group onto the X axis and the performance metrics measured on the Y axis.

![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/17e8d294-f707-441e-a969-3e15ec1f5dc6)

![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/30c32a98-0519-45ec-81e4-c3acf0bee664)

![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/bf0d14e9-c865-4b9a-85b0-d1c8bfb2eab6)

The graphs for each position all follow a very similar trend with minor nuances. Players with larger contract increases year on year are more effective than players with smaller increases or even decreases. This indicates that the sports analysts are doing a great job in valuing player contracts based on their performance. However, in some cases players seem to be slightly overvalued. This can be seen in the graph for centers which shows a decrease in rebounding after a 20 million dollar contract increase. Player performance isn't everything either, in the following graph it is clear that there is strong negative correlation between a players plus minus and a players contract increase for guards.

![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/153a0a4c-e803-4813-8827-2c7b4a756f43)

In conclusion, a players contract increase does correlate with player performance, but it does correlate to team performance.




Performance metrics as it relates to contract valuations:

This final question is best answered using a pair plot to compare a players plus minus, which is there actual value a player gives to the team, and a players contract value, which is there expected value. This should be looked at for each position. The values in the row ContractY2 (2024 NBA Season) show how a player is assigned value, the closer a performance metric such as Points Per Game is to 1 the more this stat is weighted in a contract decision. In the Plus Minus row the actual impact of each performance metric is shown. Putting these two side by side gives a great comparison of contract value compared to actual value. Theoretically, the most correlated performance metric on Plus Minus should also be the most correlated metric in Contract Value.

Guards:
![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/1b397abc-3c4a-4b25-a457-4380ccdc60c7)

For guards, the top three actual performance metrics are Field Goal Percentage, Blocks Per Game, and Steals Per Game. These are the lowest in the assigned value by a large margin which indicates that there is a mismatch for guards and their contracts. It also likely means that guards bring a different value to a team than just statistics that are shown on paper.

Forwards:
![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/ea4aa1cd-3480-4407-a58e-dc7505e7f30a)

The number one performing metric for forwards is indicated to be Field Goal Percentage. This metric has little impact on a players contract value. The next three top performing metrics, points, rebounds and assists are valued most in a forwards contract. This indicates that these contracts are on track with player performance.

Centers:
![image](https://github.com/robbinsc4ATWIT/DataScienceProject/assets/90586029/45f32e41-2ddf-49be-b145-d63ef278886b)

Centers show a large variety of performance metrics correlating with Contracts, however, there are two metrics that are significantly more important than the rest when it comes to actual performance. These metrics are points and assists. Center contracts should be slightly more tailored to centers who can perform these attributes more effectively.

# Discussion
The answers to these research questions indicate that there is more analytical work that can be done on player performance and how that will relate to a contract. A player should have better output if they have a larger contract, but the same metrics valued in plus minus are not valued equally in contracts. Designing a player contract has many nuances, and a players ability can change depending on the team around them and how they like to play. However, there are core statistics that have a larger impact on a players output than what is currently valued in contracts. The main example of this is Free Throw Percentage and Steals. These consistently have an impact on a players output but are somewhat neglected in contract valuations. More data points are necessary to give a complete scope of what a contract should value. In further research I would look more advanced statistics such as Offensive rebounds. I would also see how contract increases, especially the largest contracts of the league, relate to games won and championships won. Another question I would be interested in is if a player is in a contract year, meaning they are in the first or last year of their contract, do they perform better individually? This question revolves around the idea of pressure and how that can impact a player. 


