# My Project
This project essentially aims to to display past performance of users,display performance gap and highlight strong and weak areas for the user using data-driven insights via effective data analysis and manipulation.It also stored the input data as it will serve as historic data for future inputs.

# Datasets

The datasets used in this project are:

1)combined_file csv-This dataset is responsible for converting the Json data from https://api.jsonserve.com/XgAgFJ

2)preprocessed.csv-This dataset drops duplicates, handles missing value and drops colums with 0 unique values as there is no point in comparing.

3)sorted_data.csv-This dataset sorts the topics in order of their attempts based on start and end time of the given quiz

# Notebooks
The Jupyter Notebooks and the functions they provide:

1)Json_to_csv:This notebook is essentially converts all the json data into csv.



2)Data Insights-This jupyter file logically combines connected csvs.Then it works on that data to handle missing values, drop non-important columns,derive a number of performance features and plot them against topic and other paramters to find out data trends and insights.

-Created a logical csv by merging the response data csv and quiz data csv derived from Json data.

-Extracted topic rank and converted the topics into similar format in terms of case

-Dropped null columns,renamed duplicate columns,removed one duplicate column,dropped columns with no unique values

-Derived 3 new performace paramters-percentage,rank fraction,mistake ratio

-Nextly, I added a column which keeps a track of the number of attempts for the same topic(column:'name').The number of attempts was decided by sorting the started at time of a particular quiz meaning that quiz was attempted first(given that you cannot switch between quizes before submitting the current one).

-Lastly I plotted all the performance parameters(accuracy,percentage,mistake_ratio,rank_ratio) against topics, accuracy and difficulty level(speed)

-The topic labels also had number of attemopt  attched to it so attemots of similar quizzes can be compared



3)Execution(Most Significant):
-The user inputs their quiz results in a given format.

-The project generates performace gap of all historical data for that topic of quiz and highlights the performance gap between current attempt and all previous attempts combined.

-It generates graphs showing all the performance level ups and down occured in the previous attempts as well as current one via line graph for all parameters.

-It also is mindful of the attempt user is asking the performance of and adds it into its historical data for showcase of all the previous performance for a particular topic.

-It also highlights the if the topic and the quiz is a weak area or a strong area based on the latest attempt of the quiz.


## Possible Enhancements

(Could be done more with time)

-Final enlisting of strong and weak areas can be done for all topics and not the one that's attempted

-The parameters for performace to be good or bad are decided on a general basis.More help from domain experts could enhance the conversion of numerical parameters into strong or weak.

-The spectrum can be enhanced with larger range of feeback(for eg. very weak, weak,average,strong,very strong)

-The duration taken for quiz and speed can be related with accuracy to tell user if he/she's too fast or slow.

## Install Requirements

To install all the required dependencies for this project, use the following command:

```bash
pip install -r requirements.txt

