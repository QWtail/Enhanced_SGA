# Graph based anomaly detection

This project including 3 modules.  The obective of the code is to detect the anomaly user everyday based on their activities.

The three modules listed follow should run consecutively one after another. The output of front module will be the input of following module(s).

* Data perprocessing
* Graph analysis
* Anomaly analysis


## Software Requirement and Dependencies
### Python (>3.4)
```
Please find the dependencies in requirements.txt
```

## Directory Stucture 
* Graph_based_anomaly_detection # main folder 
  - 1_data processing # data processing module: 
    Take input from the raw dataset and output the initial attributes. After change the variables in userList.py under main folder:
    ```
    run ./code/generate_X_and_LX_initial.py 
    ```
    The initial attributes for P3 P4 and P5 are under each folder

  - graph analysis # graph module: take input from data processing module and output graph     attribute
|    |    | -- codes # scripts for calculating the correlation graph matrix and outputing graph         attributes,  refer to“Readme.txt” for details
|    |    | -- Output 
|    |    |    | -- Combined_X # userwise *.csv, observations of raw attributes
|    |    |    | -- Combined_LX # userwise *.csv, observations of graph attributes
|    |    |    | -- graph_anomaly_weight.csv # weight for graph attributes in determing the             integrated anomaly score
|    |    |    | -- G.pickle # correlation graph matrix
|    | -- anomaly analysis  # prediction module: take input from graph analysis module and         output anomaly score
|    |    | -- code # scripts of the prediction model and calculation of anomaly score,  refer         to“Readme.txt” for details
|    |    | -- results
|    |    |    | -- X # prediction error for raw attributes
|    |    |    | -- LX # prediction error for graph attributes
|    | -- dashboard    # visulization module: take input from anomaly analysis module and generate     a web-based dashboard
|    |    | -- dash_demo_dso.py # main file,  refer to“Readme.txt” for details
|    | -- README.docx # this file



## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.



