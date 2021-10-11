Amazon Rekognition Webcam Demo
==============================

This demo illustrates the [Amazon Rekognition][1] capabilities when detecting faces and labels through your computer's webcam. For that, we are going to use the [AWS SDK for Python (boto3)][2] and the [Rekognition Image API][3]. You will also need Python>=3.6 installed.


## Setup

You are going to need the [boto3][4] and [opencv-python][5] packages. For better compatibility, you can install the exact same library versions used during the development of this demo running:

    pip install -r requirements.txt

Make sure you have also configure the [authentication credentials][6] on your computer.

## Running

There are two demo scripts for you to test Amazon Rekognition.

1. The `faces_demo.py` is going to open your webcam and show gender and age information of the detected faces. To run it, use:

        python faces_demo.py

2. The `labels_demo.py` is going to open your webcam and show detected objects with bounding boxes. It is important to put here that some objects are not going to be highlighted, since not every label detected by Rekognition has an associated bounding box. Without any arguments, this script is going to show all objects that have a bounding box:

        python labels_demo.py

    You can also select a set of desired labels by using the argument `-l` (labels names are case-sensitive and quotes are needed for labels made up with two or more words):

        python labels_demo.py -l Person "Mobile Phone" Glasses


[1]: https://aws.amazon.com/rekognition/
[2]: https://boto3.amazonaws.com/v1/documentation/api/latest/index.html
[3]: https://docs.aws.amazon.com/rekognition/latest/dg/API_Reference.html
[4]: https://pypi.org/project/boto3/
[5]: https://pypi.org/project/opencv-python/
[6]: https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html#configuration
