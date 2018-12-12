# TransferLearning-with-Keras-on-TensorFlow

## Required libraries

- cv2 3.2.0
- keras 2.0.9
- matplotlib 2.1.0
- numpy 1.12.1
- sklearn 0.19.1
- tqdm 4.11.2
- PIL 4.2.1

## Motivation

I will show how to do transfer learning with Keras on TensorFlow by implementing an image classification application. Transfer Learning is an useful method when you implement Convolutional Neural Network (CNN) to classify some images. By using the method, you don’t only need to reinvent the wheel, but also save your precious time!

## A summary of result

| Model | Macro F1 | Time/Epoch | Note |
|-----|-----|-----|-----|
| A CNN from Scratch | 0.0516 | 73s |  |
| A CNN by using ResNet-50 features | 0.7972 | 2s | Transfer Learning |
| An optimized CNN by using ResNet-50 features | 0.8142 | 2s | Transfer Learning |

Not only the metric is improved by using transfer learning, but also time per epoch is surprisingly reduced. The reason for time reducing is due to the effects of a number of parameters had to be trained. In transfer learning, the output layer only have to be trained, so a number of parameters is less than the model from scratch.

Note: In our application, we classifiy image into 133 dog breed categories. When we classify one breed one-vs-rest method is used, a and lables are unblanced though numbers of each labels are almost same. So we use macro f1 score to evaluate CNN of dog breed.

## Files

- dog_app.ipynb: It describe how to do transfer learning with Keras on TenworFlow.
- dog_app.html: As the same of above notebook but format is html.

## Blog post

- https://medium.com/data-science-in-idleness/transfer-learning-with-keras-on-tensorflow-39f4bec9f420

## Acknowledgements

- I wish to thank [Udacity](https://www.udacity.com/) for datasets, advice and review.
