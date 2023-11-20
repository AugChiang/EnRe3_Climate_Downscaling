# EnRe3_Climate_Downscaling
An Encoder-Resolver model of Climate Downscaling of ERA5 </br>

training data: ERA5 in Taiwan region with the shape of (14,9)</br> 
auxiliary data: ERA5 10 meter high wind field vector u,v near Taiwan region with the shape of (14,9)</br>
label data: TCCIP grid daily precipitation with the shape of (70,45) (resized)</br>

# Model Architecture
Encoder involves Multi-head Attention Layer and Fully Connected Layer (FC). </br>
Resolver involves Upsampling Layer with Efficiency Sub-pixel method (of ESPCN) and convolutional layers. </br>
![image](https://github.com/AugChiang/EnRe3_Climate_Downscaling/blob/main/arch.png)

# Model Prediction
Prediction of precipitation on 2019.08.15 </br>
left-top: ERA5 Reanalysis Data of Precipitation </br>
left-bottom: TCCIP gridded observation </br>
right-top: MAE error heatmap </br>
right-bottom: model prediction </br>
![image](https://github.com/AugChiang/EnRe3_Climate_Downscaling/blob/main/res/20190815.png)
