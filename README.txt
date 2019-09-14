Project 1: Supervised Learning
##############################
GT CS7641 Machine Learning, Fall 2019
Eric W. Wallace, ewallace8-at-gatech-dot-edu, GTID #

## Background ##

...

## Instructions##
1. Clone this Git repository to your local machine.
2. Create a folder named "data" underneath the repository folder.
3. Prepare the Weka software:
   a. Download and install the latest stable version of Weka for your platform (version 3.8.3 or higher) from .
   b. Launch Weka, and use the Package Manager to install the following additional packages:
      - WekaExcel?
      - thresholdSelector?
4. Prepare the first data set:
   a. Download the file "default of credit card clients.xls" from the UCI Machine Learning Repository at http://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients
   b. Open the XLS file with Microsoft Excel or an online service, and edit as follows:
      1. Delete the entire 2nd row (which contains "ID, LIMIT_BAL, EDUCATION...").
      2. Delete the entire 1st column (which contains the ID numbers for each instance).
   c. Save into the "data" folder in the Comma-Separated Values (CSV) format with the filename "creditcards.csv".
   d. Launch Weka to the KnowledgeFlow GUI
      1. Open the file "_data1_prep.kf".
      2. On the "Run" tab, press the "Start" button and wait for it to complete.
      * If there's an error finding the file, you may need to edit the "ArffLoader" component to browse for the source data file due to Weka's inconsistent handling of relative file paths.
   e. Confirm that it has created a file named "creditcards.arff" in the "data" directory.
4. Prepare the second data set:
   a. Download the file "default of credit card clients.xls" from the UCI Machine Learning Repository at http://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients
   b. Save into the "data" folder in the Comma-Separated Values (CSV) format with the filename "creditcards.csv".
   c. Launch Weka to the KnowledgeFlow GUI
      1. Open the file "_data2_prep.kf".
      2. On the "Run" tab, press the "Start" button and wait for it to complete.
      * If there's an error finding the file, you may need to edit the "ArffLoader" component to browse for the source data file due to Weka's inconsistent handling of relative file paths.
   e. Confirm that it has created a file named "htru_std.arff" in the "data" directory.
5. ...
