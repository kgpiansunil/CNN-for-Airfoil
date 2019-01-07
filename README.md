# CNN-based aerodynamics parameters prediction method
CNN for airfoil lift-to-drag-ratio prediction

This repository contains data, code, and results for implementing a airfoil lift-to-drag ratio prediction method based on Convolutional Neural Network. The network model can take into cnn model `the airfoil contour` and predict its `areodynamics parameters` such as lift-to-drag ratio.  
## _What we achieved:_   
**Data Pre-processing:** raw_data_parsing.py provided a way to transform the inconsistent raw coordinates data into dimension-unified matrices, this actually gives birth to a new easy-to-process upgraded version of UIUC dataset.  
**Model building:**   This CNN models runs 5000 times faster than commercial CFD software with relative low error (i.e Test MSE 0.36 after 200 epoch's training)
## How to run  
Be sure to install Pytorch (GPU version recommended) environment with numpy, scipy and matplotlib packages.
```python
python CNN.py
```

## _Contents_  
**/data/raw_data/foil_figure.rar:**   
&emsp;a file of all filled-in grayscale airfoil contour figures generated from coordinates txt files from [UIUC Airfoil Data Site](https://m-selig.ae.illinois.edu/ads/coord_database.html).  
**/data/raw_data/csv.zip:**  
&emsp;a file of all samples' lift-to-drag ratio calculated by Xflr5
**/data/parsed_data/1_300.mat**  
&emsp;the above raw data is parsed into .mat file for loading  
**/source/raw_data_parsing.py**  
&emsp;This .py file shows steps of building a NIST36-alike organized dataset from raw data  
&emsp;Please unzip 1_300.mat and modify directory and then run it. You can pass all data, which is a 4.2 GB 1_1550.mat file.  
**/source/CNN.py**  
&emsp;Run this file to load, train and print testset result  
![](https://github.com/ziliHarvey/CNN--based-aerodynamics-parameters-prediction-method/raw/master/cnn.png)    
## Licence  
The source code is released under MIT Licence.  
This research is led by Haolin Liu, Zi Li and Fei Lu.  
Please cite properly when refer to our contents and parsed dataset in the report.  
Welcome to contact me at zili@andrew.cmu.edu for any question or suggestion.
