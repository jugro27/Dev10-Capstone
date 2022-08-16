# Predicting School District Dropout Rates 
### Group Members: Azure Eller, Juliann Groglio, Seungmin Kim, Widnie Dorilas

Dropout rates are not only an indicator of the overall health of a school district, but also directly influence the amount of funding that a school recieves as funding is primarily based on the number of students within said school. It is in everyone's best interest (the students, teachers, and even governing bodies) to create the conditions that are necessary for low dropout rates. This repository takes an in-depth look at a variety of conditions that affect dropout rates in New York State, most notably: racial makeup of school districts, allocation of financial resources, and gender distribution of school districts. We analyzed each of these conditions and their relationship with dropout rates, and we created a machine learning model that predicts the dropout rate for a school district based on all of the features within the data.

## At a glance:
It is recommended that the user look at the PowerBi Report located in the Dashboard folder, as it provides an overview of some of the most important features along with their relationship to dropout and graduation rates. The report also provides the user with some general statistics for New York State School districts. The powerpoint file and the executive summary (located in the project specifications folder) also provide an overview of the project as well as list the important questions we wished to answer through our exploration, data analysis and machine learning.

## In depth:
The technical report is the best place to start for an in depth view of the entire repository. The rest of the repository contains individual files that have a specific purpose.

### In the project specifications folder the user will find:

1. **CapstoneDatasets.pdf** - A list of all of the datasets used in the project
2. **DashboardNapkinsandFeedback.pdf** - Initial drawings of the powerBi Report and feedback from other group members
3. **VisualizationsNapkinandFeedback.pdf** - Initial drawings of specific visualizations and feedback from other group members
4. **Group4ExecutiveSummary.pdf** - Executive summary for the project, listing motivations and exploratory questions
5. **ProjectPlanBacklog.pdf** - A list of action items for the project, along with importance rank and assignment
6. **RepeatableETLreport.pdf** - A report on the data extraction, transformation and loading for the 3 datasets. Step-by-step and repeatable.
7. **ServiceDiagram.pdf** - A diagram explaining the data flow and overall relationship between data service elements

### In the Code folder the user will find:

1. **DDL.pdf** - The data definition language that we used to create the relational SQL database
2. **Machine Learning.ipynb** - Training and optimization of the machine learning model, as well as a block that exports the model as a .model file into the current user directory.
3. **School-finances-data-final.ipynb** - A jupyter notebook style databrick containing all of the data cleaning for the datasets
4. **School-finances-producer.ipynb** - A kafka producer databrick that creates a "school-finances" topic and sends one message per row of the census dataset to the school-finances topic
5. **School-finances-consumer.ipynb** - A kafka consumer databrick that consumes all of the census data messages from the school-finances topic, and compiles it into a dataframe, and writes that along with the other two cleaned datasets to the SQL server.
