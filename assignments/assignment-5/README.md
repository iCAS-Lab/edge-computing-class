# Project 5: Single Izhikevich Neuron and Synapse Simulation

[CSCE 790: Neuromorphic Computing](https://www.icaslab.com/teaching/csce790nc)  
Instructor: [Dr. Ramtin Zand](https://icaslab.com)  
Term: Spring 2024   
Assignment Author: [Peyton Chandarana](https://peytonsc.com)

---

## Assignment Summary

In this project, students will implement a single Izhikevich neuron which has one weighted input synapse and one output synapse. The goal of this assignment is for students to create input spiketrains, convert spikes into a synaptic response current, update the membrane potential, and fire any output spikes if the membrane potential of the Izhikevich neuron exceeds the voltage threshold.

---

## 0. Preliminaries

A conda environment .yml file has been provided that lists all of the necessary dependencies. Students can import the conda environment by running:

`conda env create -n project5 --file project5.yml`

The `main.py' Python script has been provided with some boilerplate functions to help students know what to implement.

The provided `main.py` also contains some utility functions for Poisson spiketrain generation and plotting the final results. A sample of the expected outputs have been provided inside the `./expected_results` directory. The `expected_behavior.png` shows a sample of the system's expected behavior as a result of the included `plot()` function. The `expected_history.csv` file is generated by the `to_csv()` function and shows a sample log of the neuron's states at each timestep of the same simulation as seen in the `expected_behavior.png` figure.

---

## 1. Variables to Experiment With

- `sim_t`: simulation time.
- `lam`: the lambda paremeter for the Poisson distribution.
- `tau`: membrane time constant of the synaptic response current.
- `Vth`: spike threshold for membrane potential.
- `w`: input synapse's weight.

Keep in mind that you are responsible for implementing and tuning all of the other neuron-specific variables for the Izhikevich model.

---

## 2. Functions to Implement

- `spike_threshold`: membrane potential threshold function.
- `src`: synaptic response current.
- `theta`: unit step function a.k.a. Heaviside step function.
- `Izh`: Izhikevich neuron model.

After you implement these function for these functions you will need to call the functions inside the time simulation loop and use the provided numpy arrays for storing a history of the state variables.

---

## 4. Submission

Your submission for this assignment should include the following:

1. Your `main.py` code which implements the functionality of a single input synapse that transmits a Poisson spiketrain, converts the spikes into a synaptic response current (SRC), updates the Izhikevich neuron's membrane potential with the SRC, and outputs spikes when the membrane potential exceeds the voltage threshold.
2. A single example plot of your system working.
3. A short write-up in PDF format that describes how you implemented your project, any challenges you encountered, and a description of how to run your code. Your write-up should be submitted as a **_PDF_** and should be written in the style of a professional paper. In other words, your submission should include an abstract, introduction, methodology, results, and conclusion section.

**_Please submit your assignment write-up, code, and image to Blackboard._**