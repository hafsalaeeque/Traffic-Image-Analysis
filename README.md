# Traffic Image Analysis
Training a neural network on traffic images to perform binary classification as:<br>
1) **medium** congested, classified as label **0**.<br>
2) **low** congested, classified as label **1**.<br>

Here I am using [Keras](https://github.com/keras-team/keras) with [TensorFlow](https://www.tensorflow.org/) backend to demostrate transfer learning on the [traffic images API](https://api.data.gov.sg/v1/transport/traffic-images) to classify images.
Training is first done on 9 images each from each class, then we 'freeze' the *feature layers* and rebuild the model to classify the remaining images.

After 87 images were scrapped each time from the [API](https://api.data.gov.sg/v1/transport/traffic-images) on 2 different times of the day - assuming one was during **peak time** and other was during **off-peak**, they had to be manually labelled.<br>

Images have been split to train and test (validation) set in the data folder. <br>

### Files in this repository
1) [Traffic Image Scraper.ipynb](https://github.com/hafsalaeeque/Traffic-Image-Analysis/blob/master/Traffic%20Image%20Scrapper.ipynb), which scraps images from the data source.
2) [Traffic_Analysis.ipynb](https://github.com/hafsalaeeque/Traffic-Image-Analysis/blob/master/Traffic_Analysis.ipynb), which uses a simple neural network for binary image classification.
