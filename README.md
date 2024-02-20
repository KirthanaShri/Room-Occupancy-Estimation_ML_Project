# Room Occupancy Estimation

> This project explores room occupancy estimation using ML techniques, analyzing environmental sensor data to optimize energy consumption and space utilization efficiency. Employing Support Vector Machines(SVM), Logistic Regression, and Neural Networks(NN), alongside Principal Component Analysis(PCA) for dimensionality reduction, achieved a precision score of 98.7% in occupancy prediction, highlighting the role of ML in smarter infrastructure planning and resource management.


## Data Description
The dataset used in this study originates from the UCI Machine Learning repository and is credited to Adarsh Pal Singh, Vivek Jain, Sachin Chaudhari, Frank Alexander Kraemer, Stefan Werner, and Vishal Garg. The dataset is prominently featured in the research paper titled "Machine Learning-Based Occupancy Estimation Using Multivariate Sensor Nodes," presented at the 2018 IEEE Globecom Workshops (GC Wkshps).

Link: [UCI Machine Learning Repository - Room Occupancy Estimation](https://archive.ics.uci.edu/dataset/864/room+occupancy+estimation)

The dataset consists of `10,129` instances with `19` features, including time series data on `temperature`, `light`, `CO2 levels`, `PIR`, and `sound`, gathered from sensor nodes in a 6m x 4.6m room.


## EDA
- `Feature Engineering:` Combined the 'Date' and 'Time' columns to create a new 'Date_time' column that helped to categorize room occupancy into different time segments ('Morning,' 'Afternoon,' 'Evening,' 'Night') by creating `Time_of_Day` column and converted them to numerical form using LabelEncoder. The 'Date_time' column was dropped to adhere to the independence assumption, facilitating the application of ML algorithms, which perform optimally under this condition.
-  `Data Preprocessing:` High correlation among features S1_temp, S3_temp, and S4_temp, suggesting their similar impact on the target variable, thus warranting the removal of two features (S1_temp and S3_temp) to streamline the dataset's dimensionality.
