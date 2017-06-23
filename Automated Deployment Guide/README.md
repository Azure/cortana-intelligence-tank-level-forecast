# [Oil & Gas Tank Level Forecasting Solution](https://go.microsoft.com/fwlink/?linkid=831187)

This folder contains the post-deployment instructions for the deployable Tank Level Forecasting solution in the Cortana Intelligence Gallery. To start a new solution deployment, visit the gallery page [here](https://gallery.cortanaintelligence.com/solutions).

## <a name="Summary"></a>Summary
<Guide type="Summary">
Today, most facilities operate reactively to problems in tank levels. This often leads to spills, emergency shutdowns, expensive remediation costs, regulatory issues, costly repairs and fines. Tank level forecasting helps manage and abate these and other problems.

Forecasts are created by harnessing the power of real-time and historical data readily available from sensors, meters and records, which helps to:

- Prevent tank spillage and emergency shutdowns
- Discover hardware malfunction or failure
- Schedule maintenance, shutdowns, and logistics
- Optimize operations and facility efficiency
- Detect pipeline leaks and slugging
- Reduce costs, fines, and downtime

The tank level forecasting process starts at the well input. Oil is measured as it comes into the facility via meters and is sent to tanks. Levels are monitored and recorded in tanks during the refining process and then oil, gas, and water output are recorded via sensors, meters, and records. Forecasts are then made using data from the facility; for example, forecasts can be made every 15 minutes.

The Cortana Intelligence Suite is adaptable and can be customized to meet different requirements that facilities and corporations have.
</Guide>

## <a name="Description"></a>Description

#### Estimated Provisioning Time: <Guide type="EstimatedTime">20 Minutes</Guide>

<Guide type="Description">

The Cortana Intelligence Suite provides advanced analytics tools through Microsoft Azure — data ingestion, data storage, data processing and advanced analytics components — all of the essential elements for building a tank level forecasting solution.

This solution combines several Azure services to provide powerful advantages. Event Hubs collects real-time tank level data. Stream Analytics aggregates the streaming data and makes it available for visualization. Azure SQL stores and transforms the tank level data. Machine Learning implements and executes the forecasting model. Power BI visualizes the real-time tank level as well as the forecast results. Finally, Data Factory orchestrates and schedules the entire data flow.

The 'Deploy' button will launch a workflow that will deploy an instance of the solution within a Resource Group in the Azure subscription you specify. The solution includes multiple Azure services (described below) along with a web job that simulates data so that immediately after deployment you have a working end-to-end solution.

After deployment, see the post deployment instructions [here](Post%20Deployment%20Instructions.md).
</Guide>

## Solution Diagram

![Solution Diagram](https://raw.githubusercontent.com/Azure/cortana-intelligence-tank-level-forecast/master/Automated%20Deployment%20Guide/Figures/Tank%20Architecture.PNG?token=AIn4kF6iayGeZ_49xop2W_9Ypq3lttDMks5ZMbhSwA%3D%3D)

## Technical details and workflow
1.	The data feeds into the **Azure Event Hubs** and **Azure SQL** service as data points or events, that will be used in the rest of the solution flow.

3.	**Azure Stream Analytics** analyze the data to provide near real-time analytics on the input stream from the event hub and directly publish to Power BI for visualization.

4.	The **Azure Machine Learning** service is used to make forecast on the tank level of particular region given the inputs received.

5.	**Azure SQL Data Warehouse** is used to store the prediction results received from the **Azure Machine Learning** service. These results are then consumed in the **Power BI** dashboard.

6. **Azure Data Factory** handles orchestration, and scheduling of the hourly model retraining.

7.	Finally, **Power BI** is used for results visualization, so that users can monitor the tank level from a facility in real time and use the forecast level to prevent spillage.
</Guide>

#### Disclaimer

©2017 Microsoft Corporation. All rights reserved.  This information is provided "as-is" and may change without notice. Microsoft makes no warranties, express or implied, with respect to the information provided here.  Third party data was used to generate the solution.  You are responsible for respecting the rights of others, including procuring and complying with relevant licenses in order to create similar datasets.
