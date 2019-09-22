Project 1: Supervised Learning
##############################
GT CS7641 Machine Learning, Fall 2019
Eric W. Wallace, ewallace8-at-gatech-dot-edu, GTID 903105196

## Background ##

Classwork for Georgia Tech's CS7641 Machine Learning course. Project code should be published publicly for grading purposes, under the assumption that students should not plagiarize content and must do their own analysis.

The following uses the Waikato Environment for Knowledge Analysis, otherwise known as Weka, for machine learning analysis of 5 different classification algorithms, on two different datasets.

## Instructions##
1. Clone this Git repository to your local machine: https://github.com/ewall/CS7641_Supervised_Learning
2. Create a folder named "data" underneath the repository folder.
3. Prepare the Weka software:
   a. Download and install the latest stable version of Weka for your platform (version 3.8.3 or higher) from https://www.cs.waikato.ac.nz/ml/weka/downloading.html
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
5. To run the learning curve experiments:
   a. First, a disclaimer: due to limitations in the Weka workbench, comparing a trained model against the training dataset is stupidly complex, so this is an ugly workaround...
   b. Launch the Weka KnowledgeFlow program and open the appropriate *.kf files in the "learning_curves" directory. Naming convention is dataset first, then algorithm, then "curve1" or "curve2" as discussed in the next step.
   c. The first KnowledgeFlow script (e.g. "data1_ann_curve1.kf") trains the learner and saves each model into the "models" directory, as well as outputs the results for validation against the test data into the same directory. (Note that they all use the same filenames, overwriting any previous executions.)
   d. The second KnowledgeFlow script (e.g. "data1_ann_curve2.kf") loads the models from the first run, compares results against the training data, and outputs the training results into the "models" directory.
   e. Plots used in my analysis are generated in Microsoft Excel from the output provided by the Weka tool.
6. To run the experiments for hyperparameter tuning and complexity analysis:
   a. Launch the Weka Experimenter program and open the appropriate *.exp files in the "hyperparameters" directory. Naming convention is dataset first, then algorithm, then hyperparameter name.
   b. Caution, many of these require hours to execute to completion, since they compare numerous options using cross-validation!
   c. Plots used in my analysis are generated in Microsoft Excel from the output provided by the Weka tool.
7. To compute the "best" results for each algorithm:
   a. Launch the Weka KnowledgeFlow program and open the appropriate *.kf files in the "hyperparameters" directory. Naming convention is dataset first, then algorithm, then "best".
   b. Note that, even though Weka stores the random seed in the script for consistency across re-runs, running this on a different operating system or hardware than I used may produce slightly different results due to differing pseudo-random number generation.

