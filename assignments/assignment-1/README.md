# Assignment 1: Convolutional Neural Networks

[CSCE 790: Edge and Neuromorphic Computing]()  
Instructor: [Dr. Ramtin Zand]()  
Term: Spring 2024  
Assignment Authors:

- [Peyton Chandarana]()
- [Mohammadreza Mohammadi]()

## Assignment Summary

In this assignment, you will use code provided to you in the form of a Jupyter notebook to train the [LeNet-5]() Convolutional Neural Network (CNN) on the [MNIST Handwritten Digit]() dataset.

## 0. Preliminaries:

- Setup a [Kaggle]() account so that you can track you progress throughout the course.
- Fill out this form [here]() so that we have a record of your username on Kaggle for the course.
- Go to the first assignment [here]() and read through the code.\

Once all of these steps have been completed you will be added to a Kaggle group.

## 1. Running the Jupyter Notebook:

1. Open the first assignment's Jupyter Notebook [here]().

2. On the right `Notebook` panel, scroll down until you see `Notebook options`. Expand this menu if it is not expanded already.

3. In the `Accelerator` dropdown menu, ensure that `None` is selected. You will be changing this multiple times in this assignment so keep a note of where this setting is.

4. Run the Jupyter notebook to train the LeNet-5 model on the MNIST Handwritten Digit dataset.

5. Save your trained model as an `*.h5` file. This file contains the saved weights and activations for your trained model. This file allows you to use your trained model without re-training it each time.

6. At the end of the notebook, you will see the `Test Accuracy` and `Latency` sections. Record/save these two metrics for analysis later.

Now that we have trained the model and performed inference on CPUs, lets try training the neural network and performing inference on the other accelerators available on Kaggle. To do this, go back to Step 3 and select each of the following accelerators. Repeat the training and inference by re-running the notebook on all of the accelerators:

- GPU T4 x2
- GPU P100
- TPU VM v3-8

## Deliverables:

Your deliverable for this assignment will consist of a 1-2 page written analysis and summary of the assignment. Your write-up should contain the following:

- A summary of what the notebook does with enough detail that someone can use your write-up and follow along with the notebook as they run each cell and understand what each cell does.

- A table of all your training and inference results across the different devices used throughout the experiments. Your table should look like:

| Device      | Training Acc. | Training Loss | Validation Acc. | Validation Loss | Training Time | Test Accuracy | Latency | Average Latency |
| ----------- | ------------- | ------------- | --------------- | --------------- | ------------- | ------------- | ------- | --------------- |
| CPU         |
| GPU T4 x2   |
| GPU P100    |
| TPU VM v3-8 |

- You should briefly discuss the results you gathered in the table across the different hardware devices. This discussion should discuss the differences between the different devices.

- Along with your Assignment 1 report including the summary and the table and analysis you should include the model, the `*.h5` file, of the best performing model maximizing the following score:

$$SCORE = {Accuracy_{test} \over Latency}$$
