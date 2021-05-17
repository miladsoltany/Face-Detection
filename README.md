# Face-Detection
Face detection using yolov5

In this repository, I have trained yolov5s on the WIDER face dataset.
The WIDER dataset comprises of more than 30k images with more than 390k faces, each with bouding box and other various label formats.

![image](http://shuoyang1213.me/WIDERFACE/support/intro.jpg)

Facial expression classification is not in the scope of this project and it is only about detection. Therefore, all the faces have the same label which is, obviosuly, "face".

The included code, which is in form of a IPython notebook, downloads the dataset and performs preproccessing. The faces with area of less than 2 percent of the whole image are considered too small and ignored. Moreover, for each image in the dataset, the yolo required format (cls,x,y,w,h) is constrcuted and saved.

Finally, the yolov5s is trained on the dataset.
The final accuracy on the validaion dataset is 93.6%

Here are the results on some randomly downloaded data with the given model.

![download](https://user-images.githubusercontent.com/44018277/118492637-74766d00-b735-11eb-8b6c-8d8226dc4f4a.jpg)
![istockphoto-1146473249-612x612](https://user-images.githubusercontent.com/44018277/118492644-76403080-b735-11eb-9f8f-21c2ed5eefd4.jpg)

# Colab Notebook
The code needed to preprocess the data and train the model is available in the following notebook.
Set the runtime to GPU and run everything.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/miladsoltany/Face-Detection/blob/main/Face_Detection.ipynb)

# Yolo weights
The weights are also available to run using the official yolov5 code found [here](https://github.com/ultralytics/yolov5)

Download the weights: [Link](https://github.com/miladsoltany/Face-Detection/blob/main/face_detection_yolov5s.pt)
