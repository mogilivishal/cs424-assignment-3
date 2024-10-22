# Traffic Data Visualizations

## Task 1: Single view visualizations

### 1. Line Chart

![1](https://github.com/user-attachments/assets/75e20537-0377-48f9-ab11-1d1ff0e669cb)


**Description:** The visualization is a line chart that shows the average speed over the hour of day. It allows us to view and interpret the data directly. It represents the average speed trends throughtout the day

#### Attributes Being Visualized:
  - **X-Axis**: HOUR
  - **Y-Axis**: Average speed (SPEED)
 

### 2. Bar Chart

![2](https://github.com/user-attachments/assets/90848739-5109-41a5-81a2-741dab123815)


**Description:** The visualization is a bar chart that shows the top 10 most congested arterial streets. It also tells us about the streets with lowest average speeds, and traffic congestion on those streets.

#### Attributes Being Visualized:
  - **X-Axis**: Average speed (SPEED)
  - **Y-Axis**: STREET


### 3. Bubble Chart

![3](https://github.com/user-attachments/assets/4efc1111-03ad-4409-bd8c-fb6a8eb54749)


**Description:** The visualization is a bubble chart that shows the relationship between bus count (BUS_COUNT), average speed (SPEED) and segment length (LENGTH) giving us the insights how these attributes are correlated.

#### Attributes Being Visualized:
  - **X-Axis**: BUS_COUNT
  - **Y-Axis**: Average speed (SPEED)
  - **Size of Bubbles**: Segment length (LENGTH)


### 4. Box Plot

![4](https://github.com/user-attachments/assets/06794a54-105c-4625-b705-995d6a14a57e)


**Description:** The vertical box plots visualization gives the information about how speed vary from month to month which helps us to identify any potential seasonal patterns or trends. It helps us in identifying outliers and variations in speed.

#### Attributes Being Visualized:
  - **X-Axis**: MONTH (Categorical)
  - **Y-Axis**: SPEED (Quantitative)
  - **Color**: MONTH (Quantitative)


### 5. Scatter Plot

![5](https://github.com/user-attachments/assets/dee9368e-6e2d-4f94-b58f-52d7fb95efe8)


**Description:** The scatter plot visualization shows us the correlations or trends between two quantitative variables: Segment Length (LENGTH) and Speed (SPEED). It helps us in identifying any potential connections between these attributes. 


#### Attributes Being Visualized:
  - **X-Axis**: Segment length - LENGTH (Quantitative)
  - **Y-Axis**: SPEED (Quantitative)


### 6. Heatmap 

![6](https://github.com/user-attachments/assets/64545ecc-964c-4bc8-8837-0088c5be92c4)


**Description:** The visualization is a heatmap which shows the level of congestion over hours of day and days of week. It uses different color variations for congestion levels, that allows us to identify patterns and trends in congestion.

#### Attributes Being Visualized:
  - **X-Axis**: DAY_OF_WEEK (Ordinal)
  - **Y-Axis**: HOUR (Ordinal)
  - **Color**: Congestion level (Quantitative)


## Task 2: Linked view visualizations

### 1. Interactive Street Speed Visualization

![2 1](https://github.com/user-attachments/assets/4ab8cb10-abbd-4fc7-9056-f6317e66b65d)


**Description:** The visualization is bar chart created using Vega-Lite, which shows us the average speed in streets along with capability to explore individual streets.

#### Attributes Being Visualized:
  - **X-Axis**: STREET (Nominal)
  - **Y-Axis**: Average Speed - SPEED (Quantitative)
  - **Color**: Interactive
  - **Opacity**: Interactive

#### Interaction Mechanisms and Methods:
- **Mechanisms:** The visualizations offers interactivity through Selection and Tooltip. 
- **Methods:** This visualizations helps us to view, explore by comparing speed in different streets. Hovering over a bar shows us a tooltip which tells us about the street name and average speed in that specific street.


### 2. Linked Line Chart and Bubble Chart

![2 2](https://github.com/user-attachments/assets/85c1f2d2-e947-4899-8a35-159323cdf118)


**Description:** This visualization has two views: a line chart and a bubble chart, created using Vega-Lite. It tells us how average speed and the number of buses vary over the hour of day for different streets. The interactivity in the visualization allows us to explore specific streets and patterns in speed & bus count.

#### Attributes Being Visualized:
- **Line Chart:**
  - **X-Axis**: HOUR (Ordinal)
  - **Y-Axis**: Average Speed - SPEED (Quantitative)
  - **Color**: STREET (Nominal, with color scheme for each street)
  - **Opacity**: Interactive
 - **Bubble Chart:**
   - **X-Axis**: STREET (Nominal)
   - **Y-Axis**: BUS_COUNT (Quantitative)
   - **Color**: STREET (Nominal, with color scheme for each street)
   - **Opacity**: Interactive


#### Interaction Mechanisms and Methods:
- **Mechanisms:** The visualizations offers interactivity through Hover Interaction and change in opacity.
- **Methods:** The visualization enables users to compare average speed and the bus count over hour of day for different streets. When were are hovering over different streets, the opacity of selected street's data point increased to 1 making them highlighted whereas the unselected streets decreases to 0.2 making them less highlighted.


### 3. Linked Scatter Plot and Histogram

![2 3](https://github.com/user-attachments/assets/37cbff46-72cf-42e7-9240-efb310a62415)


**Description:** This linked visualization is a combination of two views: a scatter plot and a histogram. The scatter plot provides the insights about the relationship between vehicle speed (SPEED), bus count (BUS_COUNT), and message count (MESSAGE_COUNT).  Whereas the histogram tells us about the distribution of speeds, excluding missing values (NaN) and negative speeds.

#### Attributes Being Visualized:
- **Scatter Plot:**
  - **X-Axis**: SPEED
  - **Y-Axis**: BUS_COUNT
  - **Color**: SPEED (using a color scale from viridis)
  - **Size**: MESSAGE_COUNT
 - **Histogram:**
   - **X-Axis**: SPEED Binned (speed values grouped into bins)
   - **Y-Axis**: Count (number of data points in each bin)
   - **Color**: Steelblue 

#### Interaction Mechanisms and Methods:
- **Mechanisms:** The visualizations offers interactivity through Selection, Filtering and Tooltip. 
- **Methods:** The interaction first implemented is by the selection in the scatter plot. When you select a point in the scatter plot, the histogram filters and updates to show the distribution of speeds for the selected data points. This lets us know how speed values are distributed for specific subsets of the data, providing insights into speed patterns associated with bus count and message count. We have also used a tooltip so that hovering over a point displays additional information including speed, bus count, and message count.

### 4. Linked Line Chart and Heatmap

![2 4](https://github.com/user-attachments/assets/a7721504-77cc-40b6-9b5f-008043c9c4a5)


**Description:**  There are two views in this linked visualization: a heatmap and a line chart. The relationship between time (TIME) and speed (SPEED) is shown in the line chart, and the average speed distribution (SPEED) based on the day of the week (DAY_OF_WEEK) and hour of the day (HOUR) is shown in the heatmap.

#### Attributes Being Visualized:
- **Line Chart:**
  - **X-Axis**: TIME
  - **Y-Axis**: SPEED
  - **Color**: Street (with an option to select multiple streets)
 - **Heatmap:**
   - **X-Axis**: HOUR (binned)
   - **Y-Axis**: DAY_OF_WEEK
   - **Color**: Average Speed (using the viridis color scale)

#### Interaction Mechanisms and Methods:
- **Mechanisms:** The visualizations offers interactivity through Selection, Filtering and Tooltip. 
- **Methods:** The interaction first implemented is by the selection in the line chart. We can select one or more streets of interest then it will update the line chart's display. Then immediately the heatmap below updates to these selections, telling us how speed patterns change across days of the week and hours of the day for the selected streets. This allows us to explore speed variations over time and across different street segments.

### 5. Linked Bar Chart and Bubble Chart

![2 5](https://github.com/user-attachments/assets/88e49920-d4b8-437d-a0ca-cb9bbff09020)


**Description:** This linked visualization consists of a bar chart and a bubble chart to tell us about the top 10 most congested streets. The bar chart shows the streets along with their average congestion levels, while the bubble chart displays the relationship between bus counts, congestion levels, and segment length for the selected streets.

#### Attributes Being Visualized
- **Bar Chart:**

  - **X-Axis**: STREET
  - **Y-Axis**: Average congestion (SPEED)
  - **Color**: Selected streets are highlighted with a different color.
  - **Tooltip**: Hovering over a bar shows the street name and average congestion in that street.

- **Bubble Chart:**

  - **X-Axis**:  Bus count
  - **Y-Axis**: Congestion level (in speed)
  - **Color**: Segment length (color-coded by scale)
  - **Tooltip**: Hovering over a bubble reveals the street name, bus count, congestion level, and segment length.

#### Interaction Mechanisms and Methods:
- **Mechanisms:** The visualizations offers interactivity through Selection, Filtering and Tooltip. 
- **Methods:** In this linked visualization the key interaction we implemented is selection of the streets (bars) in bar chart. After which, we can see how the congestion levels in selected streets correlate with bus count and segment lengths in bubble chart. This will help us to analyze and understand what factors lead to congestion on these specific streets




## Task 3: Spatial Visualization

![3 1](https://github.com/user-attachments/assets/b0e51df6-a26d-48ed-bdb1-eb3cfd2ce7d8)


**Description:** This visualization is a combination of choropleth map of Chicago street congestion levels, line chart and heatmap. This allows users to explore and analyze relationship between time, congestion on street and day-week patterns.

#### Attributes Being Visualized

- **Choropleth Map:**

  - **Color Fill**: Street segments on map are based on congestion levels. Red color represents higher congestion.
  - **Tooltip**: Hovering over a street segment displays the street name and congestion level.

- **Line Chart:**

  - **X-Axis**: TIME 
  - **Y-Axis**: Average congestion (SPEED)
  - **Color**: Different streets are color-coded. Selected streets are highlighted and others are grey.
  - **Tooltip**: Hovering over a line shows the street name, time, and speed.

- **Heatmap:**

  - **X-Axis**: HOUR
  - **Y-Axis**: DAY_OF_WEEK
  - **Color**: Average congestion speed, represented by colors on a scale.
  - **Tooltip**: Hovering over a cell inside heatmap provides details on the hour, day of the week, and average congestion speed.

#### Interaction Mechanisms and Methods:
- **Mechanisms:** The visualizations offers interactivity through Selection, Multi-selection and Tooltip. 
- **Methods:** Here in this visualization the key interaction lies in the selection of street segments on choropleth map. By selecting streets, users can see the corresponding patterns on linked chart and heatmap. This will allow us to have in-depth analysis of congestion trends and their variations across streets, time and days of week.



## Task 4: Complex visualization

From the Assignment-1 we took Sankey plot. We selected **Sankey Plot** as it cannot be implemented using Vega-lite. We plotted between **LENGTH(segment_length)** vs **SPEED**.

#### Data cleaning, Preprocessing and filtering to meet the requirements:

* Sorting the dataframe according to the target(SPEED) column in descending order of SPEED.
* Dropped the Duplicate values from both the columns (LENGTH and SPEED).
* Used only the unique values.
* Restricted the dataframe to get only top 100 rows.
* Created a new column called value which is created with values 0, 1 and 2 (Not Congested, Congested and Extremely Congested)
  
![4 1](https://github.com/user-attachments/assets/2f915ca3-14d2-456c-9f4b-5c0a8c8131a2)

* Converted the DF to a csv
* Added all the steps performed as comments in the sankey.ipynb file.
* Used D3 to create the visualization to meet the requirements and obtain the desired viz.
* When we hover over a link in the Sankey plot we will get the segement_length --> speed and the congestion level in that particular segment.

<img width="342" alt="4 2" src="https://github.com/user-attachments/assets/8f413a9b-5809-4052-ba3f-c384d465801a">





**We hosted the visualization in GitHub.**

**GitHub hosted link** : https://hemanth-git-code.github.io/hemanth_110500.github.io/



**GitHub repo** : https://github.com/Hemanth-git-code/hemanth_110500.github.io




**Reference**: https://github.com/Hemanth-110500/visualizingGeneticMutation




#### Overview of the development process:

We divided the tasks among each other and set timeliens for completing each tasks. Initially we thought we could easily complete Task 1 and Task 2 and we should focus more on Task 3 and Task 4 as it involves spatial visualizaiton and visualizaiton using D3. But to our surprise Task 1 and 
Task 2 took most of our time as we have to install all the required dependencies for vega-lite and altair.

We started the assignment on the weeekend the assignment has been released i.e. 14/11/2023. Had a team meeting on Zoom about the tasks division and contributions to the team. Later we started working on the assignment individually and contacted each other regularly and discussed the progress. Task 1 took less time after we were able to setup the environment. Task 2 was a bit difficult as it involved creating linked visualizaitons and using altair. For, Task 3 we were able to find GeoJSON data and were able to map it to our dataset. For Task 4, we focussed on developing the visualization using D3.js, which was a learning process for our whole team. We tried to replicate the same in Jupyter notebook but were unsuccessful. But we hosted it in GitHub and provided a link to it.
