# Infromation leakage detection

The obective of the code is to detect the information leakage in user's email and attachments.


## Software Requirement and Dependencies
### Python 
```
Please find the dependencies in requirements.txt
```

## Set up and run
Please read the comments in the code for understanding

- Put protected information into *Protected* folder, the type can be:
	* Image:'jpg', 'jpeg', 'png' 
	* Document: 'doc','txt','csv', etc
- Customize two functions in *run.py* to read data from dataset:
	```
	* getAllemails(date)
	* getAllattachments(date)
	```
- Change start and end date information in *Run_leak.py* before run and detect leakage

- Output: 
  - The detect result in *Detect_csv* folder and also upload to MongoDB for view on UI

## Authors

MOSCATO P5 Team, please see top lines in each code files for the contributors who participated in each project.



