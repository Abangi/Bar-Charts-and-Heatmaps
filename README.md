# Bar-Charts-and-Heatmaps

We will work with a dataset  from the US Department of Transportation that tracks flight delays
Opening the CSV file  shows a row for each month and a column for each airline code.Each entry shows the average arrival delays(in min) for a different airline and month.Negative entries denote flights that (on average) tended to arrive early.
x=flight_data.index - This determines what to use on the horizontal axis. In this case, we have selected the column that indexes the rows (in this case, the column containing the months).
y=flight_data['NK'] - This sets the column in the data that will be used to determine the height of each bar. In this case, we select the 'NK' column.
Important Note: You must select the indexing column with flight_data.index, and it is not possible to use flight_data['Month'] (which will return an error). This is because when we loaded the dataset, the "Month" column was used to index the rows. We always have to use this special notation to select the indexing column.
We create a heatmap to quickly visualize patterns in flight_data. Each cell is color-coded according to its corresponding valuE
This code has three main components:

sns.heatmap - This tells the notebook that we want to create a heatmap.
data=flight_data - This tells the notebook to use all of the entries in flight_data to create the heatmap.
annot=True - This ensures that the values for each cell appear on the chart. (Leaving this out removes the numbers from each of the cells!)
What patterns can you detect in the table? For instance, if you look closely, the months toward the end of the year (especially months 9-11) appear relatively dark for all airlines. This suggests that airlines are better (on average) at keeping schedule during these months!
