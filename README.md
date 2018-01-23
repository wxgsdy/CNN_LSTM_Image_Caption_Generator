# CNN_LSTM_Image_Caption_Generator
## Description 
• Built the modal architecture with GoogLeNet with special attention mechanism to learn image features and 
specially designed LSTM function to decode learned features and generate captions.  
• Verified the model with different metrics like BLEU-4 and CIDER on Microsoft COCO dataset and get a 
satisfying result. 

## Demo instructions
### Environment
1. caffe and pretrained GoogleNet model
2. Tensorflow.

### Usage
1.Run the following command to retrive all the data files.

    ./download.sh 

2.Run 'caption_image.py' to load and use the saved model and use command  `python caption_image.py -i images/imgname.jpg` 
produces the caption for imgname.jpg(test image).

### Other files
1.`model.py` defines the `Model` class that contains the CNN-LSTM architecture.
2.`evaluate_captions.py` generates aggregated JSON files that can then be used for hyperparameter tuning.  
3.`image_feature_cnn.py` loads up the GoogleNet batch normalization CNN model and turns images into 1024-demension vectors.
