# Face-Image-Classification

Image recognition is an interesting topic and I am excited to exercises deep learning techniques to recognize human face image using age, gender and ethnicity attributes. Sequential models with variety of input layers were tested using Keras while compiling the model. Final face recognition shows an excellent accuracy score and acceptable MSE.

### Data

Main data set is from UTKFace which has been downloaded and made it available to use. 27304 images with five columns, it was a reasonable size dataset. Features distribution and null/missing values were checked along with features relevancy. Keras / sklearn with Convolutional Neural Network models were used to perform the tasks.
 Random samples extracted from the data set
 
![text](https://user-images.githubusercontent.com/68614187/105911814-328fb280-5ff0-11eb-8603-31f8c8d1b9df.JPG)


### Exploratory Data Analysis - Data Insight
Three target variables Age, Gender and Ethnicity are mentioned categorizing the distribution.

#### Age- Ranging from 1-116 yrs 
![text](https://user-images.githubusercontent.com/68614187/105905227-cc9f2d00-5fe7-11eb-9a45-6ac1ebb36fc5.JPG)

#### Gender - 0: Male, 1: Female
![text](https://user-images.githubusercontent.com/68614187/105910076-0bd07c80-5fee-11eb-830c-9d55ced92829.JPG)

#### Ethnicity: 0: White, 1: Black, 2: Asian, 3: Indian, 4: Other
![text](https://user-images.githubusercontent.com/68614187/105911047-5a324b00-5fef-11eb-905d-e9c2a7f13587.JPG)

### Features Relevancy 
Shows the heatmap for feature's relevancy.

![text](https://user-images.githubusercontent.com/68614187/105912618-5ef7fe80-5ff1-11eb-90f4-bd8fa4346da3.JPG)

## Deep Learning Models - Regression and Classification 
As Age is considered to be the contineous variable (Regression Problem) and Gender, Ethnicity are considered (Classification Problem) due to categorical / binary variables.

### Convolutional Neural Network - Age Prediction Model
Different batch sizes were tried as input, including 64,128,256 and 512 number of layers using 'relu' as an activation. Then image was flattened and output in a sigle layer and finally model was compiled using'adam' as an optimizer with measuring 'MSE'. 
![text](https://user-images.githubusercontent.com/68614187/105915290-23f7ca00-5ff5-11eb-96f7-d0e6ba5b58f2.JPG)

#### Loss and MSE - Age Model
![text](https://user-images.githubusercontent.com/68614187/105915462-628d8480-5ff5-11eb-96b8-bbbb16503ca2.png)

### Convolutional Neural Network - Gender Prediction Model
Similar number of input layers were used with 'simoid' as activation for binary classification. Mode was compiled using 'adam' as optimizer,  binary_crossentropy as loss function and accuracy as metrics.

![text](https://user-images.githubusercontent.com/68614187/105916353-6077f580-5ff6-11eb-82a7-8168d0fa56be.png)
![text](https://user-images.githubusercontent.com/68614187/105916455-89988600-5ff6-11eb-9f02-1757b66e3487.png)

Confusion Metrix show relatively bigger numbers for 'FP' and 'FN', which might be due to some images can't be recognized fully , i.e. kids..
![text](https://user-images.githubusercontent.com/68614187/105916539-b0ef5300-5ff6-11eb-9f56-1ab51568b0a4.png)

### Convolutional Neural Network - Ethnicity Prediction Model
Ethnicity model was tested using 'softma' as activation (for multi classification) , 'adam' as optimizer and accuracy as metrics. 
![text](https://user-images.githubusercontent.com/68614187/105917124-910c5f00-5ff7-11eb-9697-341a6a741cb4.png)

![text](https://user-images.githubusercontent.com/68614187/105917439-eba5bb00-5ff7-11eb-9de6-7b2290566121.png)

Confusion metrics show the stronger prediction in category 0, 3 and 1.

![text](https://user-images.githubusercontent.com/68614187/105917519-05470280-5ff8-11eb-99dd-7769817f2fe2.png)
