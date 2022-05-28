# organic_optical_classifier
[![DOI](https://zenodo.org/badge/468072725.svg)](https://zenodo.org/badge/latestdoi/468072725)

Python code and data used in the manuscript "Machine Learning Identification of Organic Compounds using Visible Light", by Thulasi Bikku, Rubén A. Fritz, Yamil J. Colón and Felipe Herrera.  

In the organic_optical_classifier, we have 5 Jupiter Notebooks, 1 Cross Validation Folder  and 4 excel sheets containing datasets: 
1. Refractive_index_Website__data_With_and_Without_Binning_RF.ipynb
2. Featured_Engineering_1.ipynb
3. Featured_Engineering_2.ipynb
4. Organic_up_downsampled.ipynb
5. Augmented_dataset_RF.ipynb
Excel Files:
1. ORGANIC.xlsx - Dataset obtained from Refractive Index Website
2. ORGANIC_10ATT.xlsx - Dataset obtained by Feature Engineering by merging 3 records
3. ORGANIC_7ATT.xlsx - Dataset obtained by Feature Engineering by merging 2 records
4. Organic_full.xlsx - Dataset obtained from Refractive Index Website and Sellimer Equation


**Refractive_index_Website__data_With_and_Without_Binning_RF.ipynb:** Here we have considered Organic Dataset (Refractive Index Website) and applied Random Forest using Binning (Divided entire dataset into 10 equal parts) and without Binning.
Later we have divided the dataset into 5 parts based on the wavelength like UV, Visible, Near Infrared, Infrared and Far Infrared. We have applied Random Forest and found the accuracies of instances in these regions.

**Featured_Engineering_1.ipynb:** Here we have considered Organic Dataset (Refractive Index Website), we have done the feature engineering by merging 2 records to single record, so the entire datasets reduced to half. Later applied Random Forest using Binning (Divided entire dataset into 10 equal parts) and without Binning.
Later we have divided the dataset into 5 parts based on the wavelength like UV, Visible, Near Infrared, Infrared and Far Infrared. We have applied Random Forest and found the accuracies of instances in these regions.

**Featured_Engineering_2.ipynb:** Here we have considered Organic Dataset (Refractive Index Website), we have done the feature engineering by merging 3 records to single record, so the entire datasets reduced to one- third. Later applied Random Forest using Binning (Divided entire dataset into 10 equal parts) and without Binning.
Later we have divided the dataset into 5 parts based on the wavelength like UV, Visible, Near Infrared, Infrared and Far Infrared. We have applied Random Forest and found the accuracies of instances in these regions.

**Organic_up_downsampled.ipynb:** A classification data set with skewed class proportions is called imbalanced. Classes that make up a large proportion of the data set are called majority classes. Those that make up a smaller proportion are minority classes. An effective way to handle imbalanced data is to downsample and upweight the majority class. Downsampling (in this context) means training on a disproportionately low subset of the majority class examples. Upweighting means adding an example weight to the downsampled class equal to the factor by which you downsampled. Later applied Random Forest using Binning (Divided entire dataset into 10 equal parts) and without Binning.
Later we have divided the dataset into 5 parts based on the wavelength like UV, Visible, Near Infrared, Infrared and Far Infrared. We have applied Random Forest and found the accuracies of instances in these regions.

**Augmented_dataset_RF.ipynb:** Here we have considered Organic Dataset ( Refractive Index Website and Sellmeier Equation) augmentation also improves the accuracy significantly and applied Random Forest using Binning (Divided entire dataset into 10 equal parts) and without Binning.
Later we have divided the dataset into 5 parts based on the wavelength like UV, Visible, Near Infrared, Infrared and Far Infrared. We have applied Random Forest and found the accuracies of instances in these regions.

**CROSS VALIDATION:** Cross-validation is a technique for validating the model efficiency by training it on the subset of input data and testing on previously unseen subset of the input data. We can also say that it is a technique to check how a statistical model generalizes to an independent dataset.
**K-Fold Cross-Validation**
K-fold cross-validation approach divides the input dataset into K groups of samples of equal sizes. These samples are called folds. For each learning set, the prediction function uses k-1 folds, and the rest of the folds are used for the test set. This approach is a very popular CV approach because it is easy to understand, and the output is less biased than other methods.

The steps for k-fold cross-validation are:

Split the input dataset into K groups
For each group:
Take one group as the reserve or test data set.
Use remaining groups as the training dataset
Fit the model on the training set and evaluate the performance of the model using the test set.
**Here we used k=4 and 5**
