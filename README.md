## Overview
This repository includes an explanation of the project goals, approaches, and results, as well as  example code and visual aids. Refer to this repository's **Wiki** for a detailed summary of the project.  

The original image data used in this project is HIPAA protected so it cannot be shared publicly. Because of this, the training and validation code posted here cannot be executed.  However, sample output models are available so that the aggregation code can be executed. Sample models from each institution can be found **[here](https://depauledu-my.sharepoint.com/:f:/g/personal/igriza_depaul_edu/EkzhqsNEhJJPrDqDd9YUWWABzat6rNxDfVcZePrXVHMxgg?e=U8G1fh)**. 

## local_initial
Initial training for each local model. This code constructs and fits a model for each institution. The output is the trained model weights. This code is executed once for all eight institutions, and the eight models' weights are aggregated into the global model.

This code requires the original image datasets, which cannot be shared publicly. Therefore, this code cannot actually be executed and is only an example. Sample models are provided at the link in the Overview section.

## local_iteration
Subsequent training iterations after a global model has been aggregated. It is very similar to the local_initial code. The main difference is that the most recent global model's weights are used to initialize the model before it is trained again.

This code also requires the original image data, so it is only an example.

## validation
Local model evaluation. This can also be used to evaluate the global model by changing the model directory in the code. 

This code also requires the original image data, so it is only an example.

## global_aggregation
Aggregating the local models into a global model. The aggregation is done by averaging the local models' weights layer by layer.

The data and save directories in the code are only examples. To run this code, the directories should be edited to reflect the environment you're working in. Sample models are provided at the link in the Overview section.

## data
A visualization of the image datasets used in this project.

## methodology
A visualization of the federated learning process flow employed in this project.
