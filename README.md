# TrackingWalkers-YOLOv8
[![DOI](https://zenodo.org/badge/575661270.svg)](https://zenodo.org/badge/latestdoi/575661270)
This repository includes all the datasets, codes, and other resources discussed in our paper 

[Deep Learning Based Object Tracking in Walking Droplet and Granular Intruder Experiments](https://arxiv.org/abs/2302.05425) 

regarding walking droplets and granular flow experinents. 


We provide an end-to-and tutorial in *tutorial* folder. This will walk you through all the steps from creating the dataset to training your own tracker. I tested the following steps on my linux machine with Ubuntu 22.04.1 LTS.To get started, first install conda to your system, link is  [here](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), then create/activate your environment using;


>> conda env create -f environment.yml


>> conda activate droptracker


We would like to store our dataset, tracking results, and tracking results from five SOTA trackers externally, as their combined size is approximately 7GB. To do this, use the following script to download and create three folders named *dataset*, *tracking_results*, and *sota_tracks_multiple_droplets* in your current directory. If the download script is not invoked for some reason, you can directly download them from Dropbox using the links in the output.


>> python download_data.py


Lastly, start a notebook and start working on **tutorial/tutorial.ipynb** to create your own tracker. All of the main driver functions are located in **myutils.py**. I did my best to explain every step in details. I hope you find it useful. Explantions of some of the files/folders are as follows. Note that (1),(3) and (6) will appear after running the download script above. 



1- *datasets*: all the walking droplet and granular flow experiments with original videos and annotations etc.


2- *train_results*: major results regading the model training/testing process. 


3- *tracking_results*:  real-time tracking videos as well as csv files generated out of these experiments. We highly recommend to have a look at some of them.


4- *sota_tracks_multiple_droplets*:  tracking videos carried out with five SOTA models on top of YOLOv8 detections. For simplicity, we provide the results only for two and three droplets. To generate the rest, use the the very last cell in the tutorial notebook. 

5- "yolov8_tracking" and "labelImg" are cloned from their original sources. For uniformity, we added them to our repo.


6- "best_yolov8_droplet.pt" and "best_yolov8_intruder.pt" are the YOLOv8 models we trained for walking droplet and granular flow experiments, respectively. 







Please let us know if you need any question or help. You can shoot an email to erdikara@spelman.edu.
