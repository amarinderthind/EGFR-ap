# EGFR-AP : Epidermal Growth Factor Receptor-Activity Predictor


 <p align="center">
<img src="https://github.com/amarinderthind/EGFR-ap/assets/45668229/e93c5f06-8e65-44b5-b000-52297a25effb.png" width=95% height="300">&nbsp; &nbsp; &nbsp; &nbsp;
 
 
</p>

#### How the App works

For the app to work, users should download all the files in this repository and keep them in a single folder on their local machine (Check below, how to download).

The user can then run the script 'EGFR_app.py'.
To run this script, use following command 

```
streamlit run EGFR_app.py
 ```


This will open the app on the browser on the user's local machine. The user can then upload the input file in the format specified below and click the 'Predict' button.
This will run the tool, and the user will get the desired output.

##### Steps of the pipeline

The required input is a text file containing the `SMILES notation` of the small molecules whose activity will be predicted against EGFR. The user can provide a text file as a batch containing more than one small molecule's SMILES notation.

These molecules are then subjected to the computation of the 2D descriptors using the `PadelPy module`. The user can visualize the molecular descriptors computed for the input molecules and download them in a `.csv` format. Next, the app filters the initially calculated molecular descriptors and keeps only the critical descriptors, which were found to be directing the inhibitory activity of EGFR inhibitors during model building. The app then provides these essential descriptors of a different table that the user can visualize and download in `.csv` format. Finally, this information is then utilized by the app to predict the `pIC50` for the input molecules using an extra trees regressor algorithm. The user can visualize and download the activities of the input molecules. We provide the option to calculate a variety of 2D molecular descriptors for the input molecules supplied by the user, along with their predicted activities (pIC50) against EGFR. The user can visualize or download all the output files per their requirements.


##### Input file requirements

The small molecules for which the user needs to predcit the EGFR activity should be uploaded to the app as a text file. This text file should coantin the smiles notation of the molecules. The text file can have many molecules but they should be in the `SMILES` format. Check the example file (`Input_file_example.txt`) for details.

### Download 

```
git clone <SSH> or <HTTPS>
git clone git@github.com:amarinderthind/EGFR-ap.git
git clone https://github.com/amarinderthind/EGFR-ap.git

```
