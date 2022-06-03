# organic_optical_classifier
[![DOI](https://zenodo.org/badge/468072725.svg)](https://zenodo.org/badge/latestdoi/468072725)

Python code and data used in the manuscript "Machine Learning Identification of Organic Compounds using Visible Light", by Thulasi Bikku, Rubén A. Fritz, Yamil J. Colón and Felipe Herrera.  


We have tested a few classifications on the raw dataset without any preprocessing in a previous analysis. The result in the following Table:
**Method                              Accuracy(%)             Duration to execute (in mins) ** 
**Random Forest                       88.58                     38
Gradient Boosting                   72.49                     51
SVC (Support Vector Classifier)     31.73                     76
Logistic regression                 27.60                     81**

As the  Random Forest classifier results  already have  good accuracies, we proceed to focus  our efforts on  this classifier for the rest of the work.
This Table is added to the SM as Table  S1. And the following added to the draft: **"We also tested other classifiers like Gradient boost, SVC, and logistic regression, but RF performed better, so we focused our effort on working with this method."**


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


**REFERENCES**

[1]	M. Doucet, R. K. Archibald, and W. T. Heller, Machine Learning for Neutron Reflectometry Data Analysis of Two-Layer Thin Films, Mach. Learn. Sci. Technol. 2, 35001 (2021).
[2]	D. Ratner, B. Sumpter, F. Alexander, J. J. Billings, R. Coffee, S. Cousineau, P. Denes, M. Doucet, I. Foster, A. Hexemer, D. Hidas, X. Huang, S. Kalinin, M. Kiran, A. G. Kusne, A. Mehta, A. (Timmy) Ramirez-Cuesta, S. Sankaranarayanan, M. Scott, M. Stevens, Y. Sun, J. Thayer, B. Toby, D. Ushizima, R. Vasudevan, S. Wilkins, and K. Yager, [Office of Basic Energy Sciences (BES)] Roundtable on Producing and Managing Large Scientific Data with Artificial Intelligence and Machine Learning, 2019.
[3]	Z. Ballard, C. Brown, A. M. Madni, and A. Ozcan, Machine Learning and Computation-Enabled Intelligent Sensor Design, Nat. Mach. Intell. 3, 556 (2021).
[4]	X. D. Wang and O. S. Wolfbeis, Fiber-Optic Chemical Sensors and Biosensors (2015-2019), Analytical Chemistry.
[5]	C. McDonagh, C. S. Burke, and B. D. MacCraith, Optical Chemical Sensors, Chem. Rev. 108, 400 (2008).
[6]	P. Gründler, Chemical Sensors: An Introduction for Scientists and Engineers (2007).
[7]	T. M. Swager and K. A. Mirica, Introduction: Chemical Sensors, Chem. Rev. 119, 1 (2019).
[8]	S. Mohan, E. Kato, J. K. Drennen 3rd, and C. A. Anderson, Refractive Index Measurement of Pharmaceutical Solids: A Review of Measurement Methods and Pharmaceutical Applications, J. Pharm. Sci. 108, 3478 (2019).
[9]	R. W. Boyd, Nonlinear Optics, 3rd ed. (Academic Press, 2008).
[10]	F. M. V. Pereira, A. de S. Carvalho, L. F. Cabeça, and L. A. Colnago, Classification of Intact Fresh Plums According to Sweetness Using Time-Domain Nuclear Magnetic Resonance and Chemometrics, Microchem. J. 108, 14 (2013).
[11]	L. S. Magwaza and U. L. Opara, Analytical Methods for Determination of Sugars and Sweetness of Horticultural Products—A Review, Sci. Hortic. (Amsterdam). 184, 179 (2015).
[12]	M. G. Madden and T. Howley, A Machine Learning Application for Classification of Chemical Spectra, in Applications and Innovations in Intelligent Systems XVI, edited by T. Allen, R. Ellis, and M. Petridis (Springer London, London, 2009), pp. 77–90.
[13]	H. Park and J. H. Son, Machine Learning Techniques for Thz Imaging and Time-Domain Spectroscopy, Sensors (Switzerland) 21, 1 (2021).
[14]	Y. Cao, P. Huang, J. Chen, W. Ge, D. Hou, and G. Zhang, Qualitative and Quantitative Detection of Liver Injury with Terahertz Time-Domain Spectroscopy, Biomed. Opt. Express 11, 982 (2020).
[15]	L. Zhang, C. Li, D. Peng, X. Yi, S. He, F. Liu, X. Zheng, W. E. Huang, L. Zhao, and X. Huang, Raman Spectroscopy and Machine Learning for the Classification of Breast Cancers, Spectrochim. Acta Part A Mol. Biomol. Spectrosc. 264, 120300 (2022).
[16]	E. Ryzhikova, N. M. Ralbovsky, V. Sikirzhytski, O. Kazakov, L. Halamkova, J. Quinn, E. A. Zimmerman, and I. K. Lednev, Raman Spectroscopy and Machine Learning for Biomedical Applications: Alzheimer’s Disease Diagnosis Based on the Analysis of Cerebrospinal Fluid, Spectrochim. Acta Part A Mol. Biomol. Spectrosc. 248, 119188 (2021).
[17]	A. Cui, K. Jiang, M. Jiang, L. Shang, L. Zhu, Z. Hu, G. Xu, and J. Chu, Decoding Phases of Matter by Machine-Learning Raman Spectroscopy, Phys. Rev. Appl. 12, 054049 (2019).
[18]	S. Guo, J. Popp, and T. Bocklitz, Chemometric Analysis in Raman Spectroscopy from Experimental Design to Machine Learning–Based Modeling, Nat. Protoc. 2021 1612 16, 5426 (2021).
[19]	J. C. Martinez, J. R. Guzmán-Sepúlveda, G. R. Bolañoz Evia, T. Córdova, and R. Guzmán-Cabrera, Enhanced Quality Control in Pharmaceutical Applications by Combining Raman Spectroscopy and Machine Learning Techniques, Int. J. Thermophys. 2018 396 39, 1 (2018).
[20]	M. G. Madden and A. G. Ryder, Machine Learning Methods for Quantitative Analysis of Raman Spectroscopy Data, Https://Doi.Org/10.1117/12.464039 4876, 1130 (2003).
[21]	C. Berghian-Grosan and D. A. Magdas, Application of Raman Spectroscopy and Machine Learning Algorithms for Fruit Distillates Discrimination, Sci. Reports 2020 101 10, 1 (2020).
[22]	Y. Zhang, Q. Cong, Y. Xie, JingxiuYang, and B. Zhao, Quantitative Analysis of Routine Chemical Constituents in Tobacco by Near-Infrared Spectroscopy and Support Vector Machine, Spectrochim. Acta Part A Mol. Biomol. Spectrosc. 71, 1408 (2008).
[23]	W. Hu, S. Ye, Y. Zhang, T. Li, G. Zhang, Y. Luo, S. Mukamel, and J. Jiang, Machine Learning Protocol for Surface-Enhanced Raman Spectroscopy, J. Phys. Chem. Lett. 10, 6026 (2019).
[24]	N. M. Ralbovsky and I. K. Lednev, Towards Development of a Novel Universal Medical Diagnostic Method: Raman Spectroscopy and Machine Learning, Chem. Soc. Rev. 49, 7428 (2020).
[25]	E. Guevara, J. Carlos Torres-galván, M. G. Ramírez-elías, C. Luevano-contreras, F. Javier González, F. Gutiérrez-Delgado, M. A. Lopéz-Pacheco, A. E. Villanueva-Luna, N. C. Dingari, G. L. Horowitz, J. W. Kang, R. R. Dasari, I. Barman, A. Martin, L. Pereira, S. M. Ali, C. D. Pizzol, C. A. Tellez, P. P. Favero, L. Santos, V. V da Silva, C. E. O Praes, M. Jermyn, J. Desroches, J. Mercier, M. Tremblay, K. St-Arnaud, M. Guiot, K. Petrecca, F. Leblond, M. Gniadecka, P. A. Philipsen, S. Sigurdsson, S. Wessel, O. F. Nielsen, D. H. Christensen, J. Hercogova, K. Rossen, H. K. Thomsen, R. Gniadecki, L. K. Hansen, H. C. Wulf, G. Lü, J. Tang, J. Mo, X. Lü, and Z. Gao, Use of Raman Spectroscopy to Screen Diabetes Mellitus with Machine Learning Tools, Biomed. Opt. Express, Vol. 9, Issue 10, Pp. 4998-5010 9, 4998 (2018).
[26]	T. Zou, Y. Dou, H. Mi, J. Zou, and Y. Ren, Support Vector Regression for Determination of Component of Compound Oxytetracycline Powder on Near-Infrared Spectroscopy, Anal. Biochem. 355, 1 (2006).
[27]	B. Li, M. Schmidt, and T. S. Alstrøm, Raman Spectrum Matching with Contrastive Representation Learning, Analyst 2238 (2022).
[28]	W. Zhou, Y. Tang, Z. Qian, J. Wang, and H. Guo, Deeply-Recursive Convolutional Neural Network for Raman Spectra Identification, RSC Adv. 12, 5053 (2022).
[29]	R. Zhang, H. Xie, S. Cai, Y. Hu, G. kun Liu, W. Hong, and Z. qun Tian, Transfer-Learning-Based Raman Spectra Identification, J. Raman Spectrosc. 51, 176 (2020).
[30]	M. Hamed Mozaffari and L. L. Tay, Overfitting One-Dimensional Convolutional Neural Networks for Raman Spectra Identification, Spectrochim. Acta - Part A Mol. Biomol. Spectrosc. 272, 120961 (2022).
[31]	L. W. Shang, Y. L. Bao, J. L. Tang, D. Y. Ma, J. J. Fu, Y. Zhao, X. Wang, and J. H. Yin, A Novel Polynomial Reconstruction Algorithm-Based 1D Convolutional Neural Network Used for Transfer Learning in Raman Spectroscopy Application, J. Raman Spectrosc. 53, 237 (2022).
[32]	M. López-López and C. García-Ruiz, Infrared and Raman Spectroscopy Techniques Applied to Identification of Explosives, TrAC Trends Anal. Chem. 54, 36 (2014).
[33]	M. J. Baker, H. J. Byrne, J. Chalmers, P. Gardner, R. Goodacre, A. Henderson, S. G. Kazarian, F. L. Martin, J. Moger, N. Stone, and J. Sulé-Suso, Clinical Applications of Infrared and Raman Spectroscopy: State of Play and Future Challenges, Analyst 143, 1735 (2018).
[34]	B. Schrader and D. Bougeard, Infrared and Raman Spectroscopy : Methods and Applications, 787 (1995).
[35]	C. M. Liu, L. Xu, H. Y. He, W. Jia, and Z. D. Hua, Discrimination of Phenethylamine Regioisomers and Structural Analogues by Raman Spectroscopy, J. Forensic Sci. 66, 365 (2021).
[36]	H. Park and J.-H. Son, Machine Learning Techniques for THz Imaging and Time-Domain Spectroscopy, Sensors 21, (2021).
[37]	A. R. Katritzky, S. Sild, and M. Karelson, Correlation and Prediction of the Refractive Indices of Polymers by QSPR, J. Chem. Inf. Comput. Sci. 38, 1171 (1998).
[38]	P. R. Duchowicz, S. E. Fioressi, D. E. Bacelo, L. M. Saavedra, A. P. Toropova, and A. A. Toropov, QSPR Studies on Refractive Indices of Structurally Heterogeneous Polymers, Chemom. Intell. Lab. Syst. 140, 86 (2015).
[39]	R. Bouteloup and D. Mathieu, Improved Model for the Refractive Index: Application to Potential Components of Ambient Aerosol, Phys. Chem. Chem. Phys. 20, 22017 (2018).
[40]	M. E. Erickson, M. Ngongang, and B. Rasulev, A Refractive Index Study of a Diverse Set of Polymeric Materials by QSPR with Quantum-Chemical and Additive Descriptors, Mol. 2020, Vol. 25, Page 3772 25, 3772 (2020).
[41]	P. M. Khan, B. Rasulev, and K. Roy, QSPR Modeling of the Refractive Index for Diverse Polymers Using 2D Descriptors, ACS Omega 3, 13374 (2018).
[42]	G. Astray, A. Cid, O. Moldes, J. A. Ferreiro-Lage, J. F. Gálvez, and J. C. Mejuto, Prediction of Refractive Index of Polymers Using Artificial Neural Networks, J. Chem. Eng. Data 55, 5388 (2010).
[43]	J. G. Liu and M. Ueda, High Refractive Index Polymers: Fundamental Research and Practical Applications, J. Mater. Chem. 19, 8907 (2009).
[44]	H. Redmond and J. E. Thompson, Evaluation of a Quantitative Structure-Property Relationship (QSPR) for Predicting Mid-Visible Refractive Index of Secondary Organic Aerosol ({SOA}), Phys. Chem. Chem. Phys. 13, 6872 (2011).
[45]	R. C. Chen, C. Dewi, S. W. Huang, and R. E. Caraka, Selecting Critical Features for Data Classification Based on Machine Learning Methods, J. Big Data 7, 1 (2020).
[46]	M. M. Flores-Leonar, L. M. Mejía-Mendoza, A. Aguilar-Granda, B. Sanchez-Lengeling, H. Tribukait, C. Amador-Bedolla, and A. Aspuru-Guzik, Materials Acceleration Platforms: On the Way to Autonomous Experimentation, Curr. Opin. Green Sustain. Chem. 25, 100370 (2020).
[47]	H. S. Stein and J. M. Gregoire, Progress and Prospects for Accelerating Materials Science with Automated and Autonomous Workflows, Chem. Sci. 10, 9640 (2019).
[48]	F. S. Rocha, A. J. Gomes, C. N. Lunardi, S. Kaliaguine, and G. S. Patience, Experimental Methods in Chemical Engineering: Ultraviolet Visible Spectroscopy—UV-Vis, Can. J. Chem. Eng. 96, 2512 (2018).
[49]	J. H. Wade and R. C. Bailey, Refractive Index-Based Detection of Gradient Elution Liquid Chromatography Using Chip-Integrated Microring Resonator Arrays, Anal. Chem. 86, 913 (2014).
[50]	M. N. Polyanskiy, Refractive Index Database.
[51]	A. Fernández, García, Salvador, M. Galar, R. C. Prati, B. Krawczyk, and F. Herrera, Learning from Imbalanced Data Sets (Springer, Cham, 2018).
[52]	J. Cai, J. Luo, S. Wang, and S. Yang, Feature Selection in Machine Learning: A New Perspective, Neurocomputing 300, 70 (2018).
[53]	A. Parmar, R. Katariya, and V. Patel, A Review on Random Forest: An Ensemble Classifier, in Lecture Notes on Data Engineering and Communications Technologies, Vol. 26 (Springer, Cham, 2019), pp. 758–763.
[54]	F. Pedregosa, G. Varoquaux, A. Gramfort, V. Michel, B. Thirion, O. Grisel, M. Blondel, P. Prettenhofer, R. Weiss, V. Dubourg, J. Vanderplas, A. Passos, D. Cournapeau, M. Brucher, M. Perrot, and E. Duchesnay, Scikit-Learn: Machine Learning in Python, J. Mach. Learn. Res. 12, 2825 (2011).
[55]	A. S. More and D. P. Rana, Review of Random Forest Classification Techniques to Resolve Data Imbalance, in Proceedings - 1st International Conference on Intelligent Systems and Information Management, ICISIM 2017, Vols. 2017-Janua (Institute of Electrical and Electronics Engineers Inc., 2017), pp. 72–78.
[56]	J. L. Lustgarten, V. Gopalakrishnan, H. Grover, and S. Visweswaran, Improving Classification Performance with Discretization on Biomedical Datasets, AMIA Annu. Symp. Proc. 2008, 445 (2008).
[57]	NASA ipac, Near, Mid and Far-Infrared, https://archive.ph/20120529003352/http://www.ipac.caltech.edu/Outreach/Edu/Regions/irregions.html.
[58]	A. Ali, S. M. Shamsuddin, and A. L. Ralescu, Classification with Class Imbalance Problem: A Review, Int. J. Adv. Soft Comput. Its Appl. 7, 176 (2015).
[59]	T. Howley, M. G. Madden, M. L. O’Connell, and A. G. Ryder, The Effect of Principal Component Analysis on Machine Learning Accuracy with High-Dimensional Spectral Data, Knowledge-Based Syst. 19, 363 (2006).
