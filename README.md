## README.md

#### AeroPredict: Spark-Powered Flight Delay Forecasting

AeroPredict is a cutting-edge predictive model designed to accurately forecast flight delays, facilitating better decision-making for airlines and passengers alike. By leveraging extensive datasets and advanced machine learning algorithms, AeroPredict aims to minimize the inconvenience and financial losses typically associated with flight delays in the aviation industry.

#### Team Members
- Ningyu Han
- Jiaying Liang
- Ruiqi Zhou

### Project Description

**Objective:**
Develop models to predict flight delays using historical data, helping airlines and passengers make more informed decisions.

**Impact and Application:**
This project is intended to reduce the negative impacts of flight delays by providing early predictions, thus allowing for better resource management and planning in the aviation industry.

**Data Foundation:**
The model utilizes a detailed dataset from Kaggle, which includes extensive flight records and features necessary for comprehensive analysis.  

**Data for modeling**: 
* No delayed ("Delay" = 0) [26659 rows];
* Delayed ("Delay" = 1) [26657 rows]


### Models Used

- Logistic Regression
- Decision Tree
- Random Forest Classifier
- Gradient Boosted Decision Trees (GBDT)
- Multilayer Perceptron
- Linear Support Vector Machine
- OneVsRest with AutoML

### Key Findings

- High accuracy and AUC scores indicate robust model performance.
- Feature importance analysis reveals key predictors such as temperature, wind conditions, and specific airport-related factors.

### Limitations

- Current implementation does not support job submission on cloud platforms.

### Future Work

- [Addressed] Address dataset imbalance through more sophisticated sampling techniques.
- Enhance cloud integration for scalable model training and deployment.

### Steps to follow to fully replicate the results:

- Download the data on Kaggle: [FlightQuest2DataRelease2_AggregateTrain](https://www.kaggle.com/competitions/flight2-main/data?select=FQ2DataRelease2_AggregateTrain.zip)
- Upload four data on Google Cloud Storage Bucket:
  1. training2_asdiflightplan.csv (1.57 GB, 11 columns)
  2. training2_fdwind.csv (5.4 MB, 5 columns)
  3. training2_fdwindairport.csv (60 KB, 3 columns)
  4. training2_flighthistory.csv (190 MB, 26 columns)
- Setup Google Cloud Cluster in the following steps:
  0. Choose the project you create that you put above data in
  1. Click CREATE CLUSTER -> choose Cluster on Compute Engine -> click CREATE
  2. On Set up cluster page:
       1. choose Cluster type-Single Node;
       2. Versioning-2.0 Ubuntu (at the bottom);
       3. Dataproc Metastore-select the project name for this project;
       4. Components-check the Enable component gateway;
       5. Optional components-check Jupyter Notebook
       6. Click CREATE
- Download [32_write_encoded_data_as_csv.ipynb](https://github.com/ruiqiizhou/BigDataProject/blob/main/32_write_encoded_data_as_csv.ipynb) and run the whole notebook (change the Google Cloud Bucket path to your path)
- Download [42_final_modleing_milestone4.ipynb](https://github.com/ruiqiizhou/BigDataProject/blob/main/42_final_modleing_milestone4.ipynb) and run the whole notebook (change the Google Cloud Bucket path to your path)


### Contributing

We welcome contributions from the community. Please refer to the CONTRIBUTING.md file for more details on how to submit pull requests or issues.


### Support

For support, email 
- ruiqizhou@vanderbilt.edu
- jiaying.liang@vanderbilt.edu
- ningyi.han@vanderbilt.edu
or open an issue in the GitHub repository.

---

