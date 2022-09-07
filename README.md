## Face Detect
The FaceDetect model detects one or more faces in a given image or video. Compared to the FaceirNet model, this model gives better results with RGB images and smaller faces.
The model is based on the NVIDIA DetectNet_v2 detector with ResNet18 as a feature extractor. This architecture, also known as GridBox object detection, uses bounding-box regression on a uniform grid on the input image. The gridbox system divides an input image into a grid that predicts four normalized bounding-box parameters (xc, yc, w, h) and a confidence value per output class. The raw normalized bounding-box and confidence detections need to be post-processed by a clustering algorithm such as DBSCAN or NMS to produce the final bounding-box coordinates and category labels.

## About Quick Deploy
The quick deploy feature automatically sets up the Vertex AI instance with an optimal configuration, preloads the dependencies, runs the software from NGC without any need to set up the infrastructure.


## Learning Objectives
In this notebook, you will learn how to leverage the simplicity and convenience of TAO to:

* Take a pretrained resnet18 model and train a ResNet-18 FaceNet model on the WIDERFACE dataset
* Prune the trained FaceNet model
* Retrain the pruned model to recover lost accuracy
* Export the pruned model
* Run Inference on the trained model


## Get Started with Training
To help you get started, we have created a sample Jupyter Notebook that can be easily deployed on Vertex AI using *NGC’s One Click Deploy* feature. This feature automatically sets up the Vertex AI instance with an optimal configuration, preloads the dependencies, runs the software from NGC without any need to set up the infrastructure. 

Simply click on the button that reads “Deploy to Vertex AI” and follow the instructions. 

*Note: A customized kernel for the Jupyter Notebook is used as the primary mechanism for deployment. This kernel has been built on the TAO Toolkit container.

nvcr.io/nvidia/tao/tao-toolkit-tf:v3.22.05-tf1.15.4-py3



