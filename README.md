# Speech-To-Test model for command recognition

The model was trained using a CNN architure and trained on the dataset contained in this folder.

The datasets contains single digit numbers in Bosnian language and has around 400 audio samples in wav format. The audio samples were collected either by directly recording or taking them from 
audio books/ videos. All of the audio samples are 1 second long and shall any other samples be added they shouldn't be shorter than 1 second. The data can be used for testing purposes,
however a better dataset should be used to achieve a better and more robust system. The preprocessed data for each audio sample is stored in the data.json file.
2. Training a new model

First step is to prepare and preprocess the training data. Use the prepare_dataset.py and specify the folder where your data is located. Audio samples for each digit should be 
located in separate folders. Run the prepare_dataset.py and wait for the data to be preprocessed, it should take around 1 minute to preprocess the audio samples that are currently
available. The preprocessed data for each audio sample is stored in the data.json file.

Secondly, train the CNN model by running the train.py. The trianing time depens on the hyper parameters you set, but it should't take more than 2 minutes with the parameters that
are given in the code. Finally, to manually test it, fill in the _mapping list with the digits that you trained the model on. For example, if you trained for all the digits between 
0 and 9, your _mapping  should look like this:

_mapping= [
        "0",
        "1",
        "2",
        "3",
        "4",
        "5",
        "6",
        "7",
        "8",
        "9"
    ]
