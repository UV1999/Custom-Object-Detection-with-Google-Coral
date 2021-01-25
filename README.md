# google-coral_custom_object-detection
Here, I am adopting the official Google Docker documentation tutorial but I am retaining the object detection model with my own custom dataset. This repo is for retraining an object detection model to recognize a set of classes using our very own custom dataset. All the prerequisites were downloaded and requirements were met. And as given in the tutorial, after starting the docker container, the download and configure the training data step given in the official Google-coral tutorial were skipped because we are using our very own custom dataset.

And by following the instructions given in the Google-coral website for configuring your own training data, we took our own images and labeled all those using LableMe to get the annotations in xml format. Then we converted the same to tf_record which is required to start training the model. There are a total of three classes namely person, mask, and face for which we also updated the label_map.pbtxt file. The model that we used here is the MobileNet SSD V1. The model was downloaded and we also changed the pipeline.config file pointing to our own custom tf_record, label_map.pbtxt file, and the mobilenet_ssd_v1 model checkpoint file.


Google Drive Link for dataset and TFRecord - https://drive.google.com/file/d/13aVHh6A51rMz1rP1XdlsYSbm-fc6icgZ/view?usp=sharing
Google Coral Retrain an Object Detection Model Official Tutorial - https://coral.ai/docs/edgetpu/retrain-detection/#compile-the-model-for-the-edge-tpu
