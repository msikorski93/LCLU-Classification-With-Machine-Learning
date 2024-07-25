# LCLU-Classification-With-Machine-Learning
![ alt text ](https://img.shields.io/badge/license-MIT-green?style=&logo=)
![ alt text ](https://img.shields.io/badge/-Jupyter-F37626?logo=Jupyter&logoColor=white)
![ alt text ](https://img.shields.io/badge/-NumPy-013243?logo=Numpy&logoColor=white)
![ alt text ](https://img.shields.io/badge/GDAL-5CAE58?logo=gdal&logoColor=fff)
![ alt text ](https://img.shields.io/badge/-scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![ alt text ](https://img.shields.io/badge/OSGeo-4CB05B?logo=osgeo&logoColor=fff)
![ alt text ](https://img.shields.io/badge/-pandas-150458?logo=Pandas&logoColor=white)

This notebook was created to examine the accuracy of different machine-learning classifiers for LULC mapping for satellite images. The aim was to suggest the best classifier. Four popular machine-learning algorithms were applied on the Sentinel-2 data for the LULC classification. Results suggest that the closest classifications were performed by category boosting and random forests. The mapping results of the Naive Bayes model are very generalized, yet still capable to properly classify the major land covers (permanent water bodies, grasslands, built-ups). The study proves machine-learning techniques to be very useful and accurate for land-cover tasks in remote sensing.

<p align='center'>
<img src='https://github.com/user-attachments/assets/8589d341-20c2-433d-ace0-4c15ee26570b' width='700'/>
</p>

Predicted land cover surfaces in percentage:
|                     | Tree Cover | Shrubland | Grassland | Cropland | Built-up | Bare/sparse vegetation | Waterbodies | Herbaceous wetland |
|---------------------|------------|-----------|-----------|----------|----------|------------------------|-------------|--------------------|
| CatBoost            | 19.50      | 0.01      | 37.76     | 0.03     | 12.51    | 0.32                   | 29.83       | 0.05               |
| GaussianNB          | 13.37      | 0.00      | 45.23     | 0.00     | 10.92    | 0.00                   | 30.48       | 0.00               |
| k-Nearest Neighbors | 7.00       | 0.22      | 50.92     | 0.01     | 11.82    | 0.35                   | 29.68       | 0.00               |
| RandomForest        | 16.77      | 0.01      | 40.11     | 0.03     | 12.89    | 0.30                   | 29.82       | 0.00               |

Empirical evaluation assessments were undertaken by using accuracy and the Kappa coefficient. Below are the following scores:
|               | CatBoost | GaussianNB | k-Nearest Neighbors | RandomForest |
|---------------|----------|------------|---------------------|--------------|
| Accuracy      | 0.9049   | 0.8668     | 0.9018              | 0.9027       |
| Cohen's kappa | 0.8258   | 0.7514     | 0.8205              | 0.8218       |
