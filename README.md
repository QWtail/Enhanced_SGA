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
* DSO Anomaly Dectection # main folder 
  - data processing # data processing module: take input from the raw dataset and output the initial attributes
    - DSO_file_attribute # FILE LOG
      - FileMoniter # raw data of FILE LOG from DSO 
|    |    |    | -- UserFiles # preprocessed data: input is the raw data
|    |    |    | -- Output # extracted file log attributes: input is the preprocessed data
|    |    |    | -- Code # code folder for extracting file log attributes, refer to“Readme.txt”             for details
|    |    | -- DSO_Network_attribute # NETWORK LOG
|    |    |    | -- Network_log_raw # raw data of NETWORK LOG from DSO 
|    |    |    | -- Network_log_processed # preprocessed data: input is the raw data
|    |    |    | -- Network_log_attribute # extracted file log attributes: input is the                 preprocessed data
|    |    |    | -- Code # code folder for extracting network log attributes,  refer                     to“Readme.txt” for details
|    |    | -- dso_process_attribute #PROCESS LOG
|    |    |    | -- ProcessMonitor_anonymize # raw data of PROCESS LOG from DSO 
|    |    |    | -- UserFiles # preprocessed data: input is the raw data
|    |    |    | -- Output # extracted process log attributes: input is the preprocessed data
|    |    |    | -- codes # code folder for extracting process log attributes, refer                     to“Readme.txt” for details
|    |    | -- Combined_Attribute
|    |    |    | -- Code # code folder for combining log attributes,  refer to“Readme.txt”             for details
|    |    |    | -- *.csv # userwise combined attributes
|    |    | -- department & role.csv # background info file
|    |    | -- userList.csv # background info file
|    | -- graph analysis # graph module: take input from data processing module and output graph     attribute
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


### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

