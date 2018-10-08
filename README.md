# BWSI-Medlytics
This is a new repository to be used for the BWSI Medlytics Program. This repository was used during the summer of 2018 to store data relating to atrial fibrillation (heart arryhythmias in general) of patients from multiple hospitals. Data acquired from PhysioNet (https://physionet.org/). This data set is one of many on PhysioNet. As can be seen in the repo, this dataset involved the ECGs of 8,528 patients that were classified into four different categories: no heart arrhythmia (0), atrial fibrillation (1), other heart arrhythmia(s) (2), and ECG data too noisy to analyze (3). 

An in-depth explanation of atrial fibrillation (or afib) can be found at https://www.mayoclinic.org/diseases-conditions/atrial-fibrillation/symptoms-causes/syc-20350624.

For the sake of this project, Class 3 has been removed. The main reason for this is that there is a significant accuracy gap between ECG machines and the Neulog sensors used for live demos of this algorithm. This is explained further below.

Training data has been separated from validation (and testing) data within this repo. Quantities of each set of data can be viewed here. Each identification number on each file represents one patient. Therefore, there is one .mat and one .hea file for each patient in the data collection. The .hea file contains the data in a format similar to .csv, which will be the necessary input for the algorithm.

Executive summary of project: the data from PhysioNet will be used to build a machine learning algorithm (likely a convolutional neural net) to predict whether a patient has afib (or another heart arryhthmia) based on the ECG measured. Main discrepancy to account for: patient ECG data for testing/demo purposes will be taken with Neulog sensors, not ECG machines, like the ones used to collect the data. However, it is important to note that, in application, actual ECG machines in hospitals would be used to make these diagnoses.

As of 10/05/18, this repository includes only the data used for this project. The algorithm itself is in a Colab file and will be added to this repo or a separate repo at a future date.
