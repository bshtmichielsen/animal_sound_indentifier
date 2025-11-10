# 🐏 Animal Sound Identifier
This repository contains a Jupyter notebook that serves as a practical example of how to utilize PyTorch Lightning for audio classification tasks. In this instance, we have selected a subset of [YashNita's Animal Sound Dataset](https://github.com/YashNita/Animal-Sound-Dataset), focusing on five specific animal classes: chicken, cow, donkey, frog, and sheep. To extract features from the audio data, we employ the [Librosa](https://librosa.org/doc/latest/index.html) library, which is well-regarded for its robust audio analysis capabilities. The model architecture contains two convolutional layers, each followed by a max pooling layer, leading into a fully connected layer designed to enhance classification performance. However, it is important to note that the model's accuracy is currently not satisfactory, indicating ample opportunity for improvement.

<img src="https://github.com/bshtmichielsen/animal_sound_classifier/blob/main/BANNER.jpg?raw=true" />

*Image by Stable Diffusion: a machine that can classify animal sounds*

This notebook is intentionally designed as a foundational starting point and does not strictly adhere to established best practices as it is meant as a learning opportunity. This repo belongs to a five part course: 🏠 [House Price Predictor](https://github.com/bshtmichielsen/house_price_predictor), 🐏 [Animal Sound Identifier](https://github.com/bshtmichielsen/animal_sound_identifier), 👗 [Clothing Sorter](https://github.com/bshtmichielsen/clothing_sorter),🍎 [Fruit Detector](https://github.com/bshtmichielsen/expert_chat), 💬 [Expert Chat](https://github.com/bshtmichielsen/expert_chat)

## 🎯 Learning alignments
The following aspects of machine learning are part of this example:

- Working with data files, in this case audio file
- Feature extraction using a library
- Neural Network building using layers.
- Accuracy, Precision, Recall
- Confidence scores

## 🤔 Considerations for improvement
The following is a list of considerations for improvement or for your own project.

- The train/val/test-split is random and does not guarantee that all classes are represented well in val and test. This is of a particular concern for unbalanced data (which this example has) as it is technically possible that a class does not appear in val or test and therefore the model cannot be validated or tested for that class. To counter this issue the split was made to quite largely favour the val and test proportions whereas a common practice would be to keep them smaller and have more train data.
- There is no evaluation on whether the model is overfitted, it may very well be.
- Currently only 13 MFCC features are extracted from librosa, quite likely additional features may be interesting to add.
- Adding a Confusion Matrix might be a good idea.
- more?

## ⭐ Citation & Star
If you use my work please cite and star ⭐ this repo. Thanks!

Michielsen, Bas S.H.T. (2025) "Animal Sound Classifier" GitHub: https://github.com/bshtmichielsen/animal_sound_classifier