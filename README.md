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

## Set up and run
Please read the comments in the code for understanding
* Graph_based_anomaly_detection # main folder 
  - userList.py # variables that needs to generated based on different dataset used.
    - Important: Fix this file before all modules!
  - 1_data processing # data processing module: >take input from the raw dataset and output the initial attributes. To run this module:
    - Important: The function *initial_data()* in *generate_X_and_LX_functions.py* should fit to now dataset used before run.
    ```
    run ./code/generate_X_and_LX_initial.py 
    ```
    Output: the initial attributes for P3 P4 and P5 under each folder.

  - 2_graph_analysis # graph module: >take input from data processing module and output graph attribute. To run this module:
    ```
    run ./Run_GraphAnalysis.py 
    ```
    Output: 
    - the graph attributes for P3 P4 and P5 under each folder.
    - graph_anomaly_weight.csv # weight for graph attributes in determing the integrated anomaly score
    - G.pickle # correlation graph matrix
  
  - 3_anomaly_analysis  # prediction module: >take input from graph analysis module and output anomaly score. To run this module:
    ```
    run ./Run_forecast_score_calculation.py
    ```
    Output: write to MongoDB for visulization
    - Integrated anomaly score for each user everyday during selected period.
    - Perdiction error for each group's attributes
  - Readme.md # this file

## Authors

MOSCATO P5 Team, please see top lines in each code files for the contributors who participated in each project.



