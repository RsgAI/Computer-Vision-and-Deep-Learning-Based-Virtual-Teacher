
---
# *<center>Computer Vision and Deep Learning Based Virtual Teacher</center>*

*Virtual Teacher aplication contains face recognition system and
 facial expression recognition system that uses single images as input.
 Also the aplication contains drowsiness detection system that uses sequential images as input*

### Note: Work on this project is being continued

---

# *<center>Image Classification</center>*

---

*First of all, I personally belive that it is necessary to understand the basis and philosophy of the method to be applied.
Simulating the real world in digital environment is the basis of computer science.
Many methods used in computer science are inspired by nature.
The Image Classification(Face Recognition, Facial Expression Recognition etc.) process that will be carried out within the scope of this project too will be simulate the image processing mechanism of the human brain.*

*Everything starts with how question.
How the human brain processes images?
Is the image(pixel values) taken from the human eyes really meaningful?
If a person with her/his eyes closed is given the sequential pixel values of an object, can the person recognize this object?
Or can pixel values used to describe it to someone who doesn't know what a pineapple looks like?
Sounds pretty silly doesn't it?
Things to mention instinctively to describe an object are its shape, color, texture, size etc.
We describe objects this way because that's how we actually see them and store them in our memory, not pixel values.
These are called [**Features**](https://en.wikipedia.org/wiki/Feature_(computer_vision) "wikipedia") of images or objects.
See also [**Features(Machine Learning)**](https://en.wikipedia.org/wiki/Feature_(machine_learning) "wikipedia").*

*The image processing section of the human brain is called [**Visual Cortex**](https://en.wikipedia.org/wiki/Visual_cortex "wikipedia").
If a little research is done about the Visual Cortex, it will be noticed that the image taken from the eyes undergoes many processes in Visual Cortex.
These processes can be described as [**Feature Extraction**](https://en.wikipedia.org/wiki/Feature_extraction "wikipedia") in its simplest form.
That is, the human brain processes images taken from the eyes by extracting their features.*

*[**Artificial Neural Networks(ANN)**](https://en.wikipedia.org/wiki/Artificial_neural_network "wikipedia") can be thought of as a virtual simulation of the human brain, they are frequently used in machine learning applications.
This structure has also been tried to be used for Image [**Classification**](https://en.wikipedia.org/wiki/Classification "wikipedia").
No success was achieved when a [**Feedforward Neural Network**](https://en.wikipedia.org/wiki/Feedforward_neural_network "wikipedia") was trained with image pixels.
However, successful results were achieved when the training was repeated with the features extracted from the images.
In the beginning, these features were extracted with some algorithms but this was inefficient in many ways.
First of all, these algorithms could've taken a long time to work.
In addition, the features to be extracted had to be determined manually.
This could result in ignoring many features that are valuable for the relevant classification.*

*This process continued until the [**Convolutional Neural Network(CNN)**](https://en.wikipedia.org/wiki/Convolutional_neural_network "wikipedia"), which made feature extraction a part of the learning process, which was developed by exploring the Visual Cortex at a simulable level.
See also [**Convolutional Neural Network(CNN)**](https://www.ibm.com/cloud/learn/convolutional-neural-networks "IBM"). 
Check [**This Article**](https://arxiv.org/ftp/arxiv/papers/2001/2001.07092.pdf "arxiv") for the relationship between Visual Cortex and Convolutional Neural Network(CNN).*

*Considering human experiences on this subject, visual cortex does not develop with a limited number of visuals in a limited field.
The human sees and analyzes images continuously as long as the eyes are open.
The brain, which is constantly changing, continues to improve itself by learning something new from each image.
In this way, the knowledge learned from experience in any field can be used in other fields if it is meaningful.
This is the motivation for [**Transfer Learning and Fine-Tuning**](https://www.tensorflow.org/tutorials/images/transfer_learning "tensorflow").
See also [**Transfer Learning (wikipedia)**](https://en.wikipedia.org/wiki/Transfer_learning "wikipedia")
and [**Fine-Tuning (deeplizard)**](https://deeplizard.com/learn/video/5T-iXNNiwIs "deeplizard").*

*Within the scope of this project, the architectures of [**VGG16**](https://keras.io/api/applications/vgg/ "keras") and [**MobileNet**](https://keras.io/api/applications/mobilenet/#mobilenet-function "keras")
pre-trained models will be used to be applied for the image classification processes.
See also [**MobileNet (GitHub)**](https://github.com/tensorflow/models/blob/master/research/slim/nets/mobilenet_v1.md "github") and [**Depthwise Separable Convolutions**](https://towardsdatascience.com/understanding-depthwise-separable-convolutions-and-the-efficiency-of-mobilenets-6de3d6b62503 "towardsdatascience").
See also [**VGG16 (TensorFlow)**](https://www.tensorflow.org/api_docs/python/tf/keras/applications/vgg16/VGG16 "tensorflow")*

*Many pre-trained models, including the ones to be used within the scope of this project, have been trained with (224, 224, 3) sized images containing pixel values in the [-1, 1] range.
Having the pixel values in the range of [-1, 1] ensures that the data will be symmetrical and the performance of the [**Backpropagation**](https://en.wikipedia.org/wiki/Backpropagation "wikipedia") algorithm used during training will be increased.
See also [**This Question and Answer**](https://stackoverflow.com/questions/59540276/why-in-preprocessing-image-data-we-need-to-do-zero-centered-data "stackoverflow").
Therefore, training will be performed by converting pixel values to this range with the simplest method (pixel / 127.5 - 1).*

*The same trainings will be carried out by applying [**Data Augmentation**](https://en.wikipedia.org/wiki/Data_augmentation "wikipedia") to the data in order to observe the difference.
For details of the Data Augmentation process used in this application, see also [**Image Data Augmentation**](https://www.tensorflow.org/tutorials/images/data_augmentation "tensorflow").*

---

# *<center>Components</center>*

---
## Face Recognition
An example of deep learning based face recognition.
Face recognition part of virtual teacher uses single images as input.
See [**Face Recognition Repository**](https://github.com/RsgAI/Face-Recognition "GitHub Repository") for details.

---

## <center>_I'd Be Glad If You Report Any Mistakes You Notice._</center>

---