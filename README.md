# Visual Storyteller

Image captioning project for the KIU Deep Learning course. model takes an image and generates short caption that describes it. It uses pretrained ResNet18 as encoder to get image features and LSTM as the decoder to generate caption word by word.

## Requirements

Python 3.12
torch, torchvision
pandas, pillow, matplotlib

Install with:
pip install torch torchvision pandas pillow matplotlib

## About dataset

We used the Flickr8k dataset with 8091 images, each with 5 captions. You need `captions.txt` and the `Images/` folder in the project root. These aren't in the repo because of size, so add them yourself before running.

## How to train

Open `data_and_training.ipynb` and run the cells top to bottom. It loads captions, builds the vocabulary, sets up the dataset and dataloader, then trains the encoder and decoder for 10 epochs. The trained model is saved as `model.pth`. There is also a loss curve saved as `loss.png` and experiment with higher learning rate at the end.

## How to run inference

Open `inference.ipynb` and run it. It loads `model.pth` and uses the `generate_caption(image_path, model)` function to caption images. We included few examples showing good, average and failure cases.

## Files

`data_and_training.ipynb` - data, model and training
`inference.ipynb` - loading the model and generating captions
`model.pth` - saved model and vocabulary
`loss.png` - training and validation loss

## Contributors
Giorgi Uriatmkopeli - encoder, decoder, training loop
Tinatin Khozrevanidze - dataset, dataloader, inference and results