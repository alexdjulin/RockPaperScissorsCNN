# RockPaperScissorsCNN
_My attempt at the Rock-Paper-Scissors classification problem._

![rps_title.png](medias/rps_title.png)


## Installation
```bash
git clone https://github.com/alexdjulin/RockPaperScissorsCNN.git
cd RockPaperScissorsCNN
python -m venv .venv
.venv/Scripts/activate.bat
pip install -r requirements.txt
```

## Datasets and Model
The dataset images I used to train the CNN as well as the resulting model file are too big for a git repository. You can download them here:

### Datasets
I used the following 3 datasets to train the CNN from scratch:

[DRGFREEMAN](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors)  
[SANI KAMAL](https://www.kaggle.com/datasets/sanikamal/rock-paper-scissors-dataset)  - Also available in tensorflow_datasets  
[ALEXDJULIN](https://www.kaggle.com/datasets/alexandredj/rock-paper-scissors-dataset)  -  I created this one myself.  

### Model
The most efficient version of my model is available here:  
[rps_v01_56ep_0.9641acc_0.1089loss.h5](https://www.kaggle.com/models/alexandredj/rockpaperscissorscnn)


## Notebooks description
I used the following notebooks to train and test my CNN. You will need to install Jupyter Notebook or use an extension to review them and execute the code.

- [buil_dataset.ipynb](https://github.com/alexdjulin/RockPaperScissorsCNN/blob/main/build_dataset.ipynb) - Creates Train, Test and Validation folders for you and copies all the pictures of your different datasets inside, following a given split ratio (80 / 10 / 10 for instance). Images will be renamed to avoid duplicates.
- [train_cnn.ipynb](https://github.com/alexdjulin/RockPaperScissorsCNN/blob/main/train_cnn.ipynb) - Covers all the steps needed to load and prepare your dataset, create the CNN, train it, analyse the results and test the model.
- [rps_main.ipynb](https://github.com/alexdjulin/RockPaperScissorsCNN/blob/main/rps_main.ipynb) - This is my main application to display webcam frames, create a region of interest and use the model to predict hand gestures inside it. A Capture mode lets you create new images if you want to extend a dataset or your own one like I did.
- [remove_greenscreen.ipynb](https://github.com/alexdjulin/RockPaperScissorsCNN/blob/main/remove_greenscreen.ipynb) - A notebook I wrote to remove the green background from drgfreeman's dataset images and reshape them to fit the other two.
- [remove_background.ipynb](https://github.com/alexdjulin/RockPaperScissorsCNN/blob/main/remove_background.ipynb) - A notebook I wrote to experiment removing the background from a ROI using a thresholding method. I implemented the result in my main application.
- [download_dataset.ipynb](https://github.com/alexdjulin/RockPaperScissorsCNN/blob/main/download_dataset.ipynb) - A notebook I used to download the rock-paper-scissors dataset from Tensorflow (SANI KAMAL, see link above)