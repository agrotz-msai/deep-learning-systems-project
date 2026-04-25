# deep-learning-systems-project
This my fourth project in the capstone course of Udacity's Master's Degree in AI (https://www.udacity.com/masters-artificial-intelligence). 

## Overview
In this project, we implement a deep learning experiment workflow, where we try to forecast financial timeseries obtained from Yahoo Finance (https://finance.yahoo.com). 
We will focus on daily close values for the SPX, an equity index consisting of 500 large US companies, and the VIX, an index that measures the (market expectations on the) volatility of the SPX index. 
Our goal is to forecast the daily close value for these indices on a given day from the timeseries up to that day.

We start by loading and preparing the data. We then implement and train a recurrent neural network using LSTM layers as a base model, as well as an experimental model using linear layers and ReLU activation. 
We evaluate the performance of both models on training and test data, before concluding with a short summary of our findings.

## How to run the project
The main component of the project is the Jupyter notebook 'deep-learning.ipynb'.
When checking out this repository, the dataset files 'spx.csv' and 'vix.csv' are already included.
In addition, the repository contains a 'requirements.txt' file with all required dependencies, which was generated via the command
	
	pip freeze > requirements.txt
	
It can be used e.g. in a virtual Anaconda environement by opening an Anaconda prompt window in the project directory and running the following commands:

	conda create -n env_msai_cap_4 python
	conda activate env_msai_cap_4
	pip install -r requirements.txt
	python -m ipykernel install --user --name=env_msai_cap_4
	jupyter notebook
	
The last command opens a Jupyter GUI, where one needs to click on the notebook 'deep-learning.ipynb' and then click on Run... -> Run All Cells
