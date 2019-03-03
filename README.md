# Randomized-Optimization

## Overview

This project implements 4 optimization algorithms:

- Randomized hill climbing
- Simulated annealing
- Genetic algorithm
- MIMIC

to highlight their similarity and differnece.

The first part uses RHC, SA and GA to train a neural network and compair their results with the one trained using backpropagation. The second part 
runs all 4 algorithms on 3 optimization problems:

- Continous peaks problem
- Traveling salesman problem
- Knapsack problem

to demonstrate under what problem setting does a particular optimization algorithm works well.

## Prerequites

The following libraries need to be downloaded and installed on your machine before one runs the program:

- JDK: https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html
- Apache Ant: https://ant.apache.org/bindownload.cgi
- ABAGAIL: https://github.com/pushkar/ABAGAIL

Once the above libraries are installed, do the following:

1. Modify the following code
    - phishing_nn_RHC.java
    - phishing_nn_SA.java
    - phishing_nn_GA.java
    - phishingwebsite_finaltest.java

    and make sure the PhishingWebsitesData_preprocessed.csv can be properly read by the program. 

2. Run the following prompts at command line to compile programs
    - javac phishing_nn_RHC.java
    - javac phishing_nn_SA.java
    - javac phishing_nn_GA.java
    - javac phishingwebsite_finaltest.java
    - javac ContinuousPeaks_Toy.java
    - javac TravelingSalesman_Toy.java
    - javac Knapsack.java
   
    and then move all the class files to ABAGAIL/src/opt/test

## Part 1. Training neural net with optimization algorithms

Navigate to the ABAGAIL root directory, then do the following from command line:

- ant
- java -cp ABAGAIL.jar opt.test.phishing_nn_RHC
- java -cp ABAGAIL.jar opt.test.phishing_nn_SA
- java -cp ABAGAIL.jar opt.test.phishing_nn_GA
- java -cp ABAGAIL.jar opt.test.phishingwebsite_finaltest

You can see the results for each algorithm on command line, also an output csv file is generated and located at ABAGAIL/Optimization_Results

## Part 2: Optimization problems

3 optimization problems are presented to highlight the difference between random search algorithm. From ABAGAIL root directory, run the following prompt
on command line to run the model.

1. Continuous peaks problem (SA)
  
    java -cp ABAGAIL.jar opt.test.ContinuousPeaks_Toy
  
2. Traveling salesman problem (GA)

    java -cp ABAGAIL.jar opt.test.TravelingSalesman_Toy

3. Knapsack problem (MIMIC)

    java -cp ABAGAIL.jar opt.test.Knapsack

Similar to problem 1, you can see the results at command line and in the folder ABAGAIL/Optimization_Results.

