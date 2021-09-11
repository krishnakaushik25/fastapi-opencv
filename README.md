# fastapi-opencv

Deploy an Image detection FastAPI API using Amazon ec2

In this project, there are predominantly four steps:

* Setting Up an Amazon Instance
* Creating a FastAPI API for Object Detection
* Deploying FastAPI using Docker
* An End to End App with UI


- An image is just made up of bytes, and we can encode these bytes as a string. We will use the base64 string representation, which is a popular way to get binary data to ASCII characters. And, we will pass this string representation to give an image to our API.
 
 
- Created an object detection API that makes use of this image as a string and outputs the bounding boxes for the object with the object classes as well.

Here, I used a Pytorch pre-trained fasterrcnn\_resnet50\_fpn detection model from the torchvision.models for object detection, which is trained on the COCO dataset to keep the code simple, but one can use any model. 
You can look at these posts if you want to train your custom [image classification](https://towardsdatascience.com/end-to-end-pipeline-for-setting-up-multiclass-image-classification-for-data-scientists-2e051081d41c) 
or [image detection](https://lionbridge.ai/articles/create-an-end-to-end-object-detection-pipeline-using-yolov5/) model using Pytorch.


- Create a UI based app using [Streamlit](https://towardsdatascience.com/how-to-write-web-apps-using-simple-python-for-data-scientists-a227a1a01582) using our FastAPI API.


 Works well with user-uploaded images as well as URL based images.

![](https://mlwhiz.com/images/deployment_fastapi/23.png)![](https://mlwhiz.com/images/deployment_fastapi/24.png)




Huge Thanks to this [MLWHIZ blog](https://mlwhiz.com/blog/2020/08/08/deployment_fastapi/)
