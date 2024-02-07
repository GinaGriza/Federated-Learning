# Federated-Learning
This repository includes an explanation of the project goals, approaches, and results, as well as  example code and visual aids.

The original image data used in this project is HIPAA protected so it cannot be shared publicly. Because of this, the training and validation code posted here cannot be executed.  However, sample files of model weights generated from the image data have been included, so the weight aggregation code can be executed.

The data and save directories in the code are only examples. To run the aggregation code, the directories should be edited to reflect the environment you're working in.

## local_initial
The initial training for each local model. This code constructs and fits a model for each institution. The output is the trained model weights. This code is executed once for all eight institutions, and the eight models' weights are aggregated into the global model.

This code requires the original image datasets, which cannot be shared publicly. Therefore, this code cannot actually be executed and is only an example. Sample outputs are posted in this repository.

## local_iteration
The code for subsequent training iterations after a global model has been aggregated. It is very similar to the local_initial code. The main difference is that the most recent global model's weights are used to initialize the model before it is trained again.

This code also cannot be executed without the image data, so it is only an example.

## validation
The code used to perform "internal" validation on local models. This can also be used to perform "external" or "internal" validation on the global model by changing the directories of the model and/or the validation data. 

## global_aggregation
The code used for aggregating the local models into a global model. There were a few experiments with the best way to aggregate weights, but in this code they are simply averaged.

## data.pdf
A visualization of the image datasets used in this project.

## methodology.pdf
A visualization of the federated learning process flow employed in this project.
