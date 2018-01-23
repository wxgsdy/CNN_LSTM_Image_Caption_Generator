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

2.Run  'caption_image.py' to load and use the saved model.    

We have included a demo pizza image at images/pizza.jpg to sanity 
check your installation. Running `python caption_image.py -i images/pizza.jpg` 
produces the caption "a pizza with cheese and cheese on a table". It's not perfect, but still pretty cool!

### Other files
`model.py` contains the `Model` class that contains the CNN-LSTM architecture (using Tensorflow's dynamic_rnn API) and various helper functions for generating captions. `evaluate_captions.py` is a helper script to generate aggregated JSON files that can then be used for hyperparameter tuning. `image_feature_cnn.py` contains the helper functions we use to load up the GoogleNet batch normalization CNN model and turn images into 1024 x 1 vectors.
