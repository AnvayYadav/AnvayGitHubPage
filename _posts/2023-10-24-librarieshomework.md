---
toc: true 
comments: true 
layout: post 
title: 3.14 Libraries
description: 3.14 Libraries
type: hacks
courses: { compsci: {week: 9} } 
---

1. Research 3 different libraries in Python. Explain their purpose as well as two of your favorite variables/functions in each.

a. NumPy:
Purpose: It provides support for arrays and matrices, along with mathematical functions to operate on these arrays.

numpy.array(): This function creates a NumPy array from a list.

numpy.mean(): It calculates the mean of the elements in an array.

b. Pandas:

Purpose: Pandas is a library for data manipulation and analysis, and is overall very efficient.reversed

pandas.DataFrame(): This constructor is used to create DataFrames.

DataFrame.describe(): It generates descriptive statistics of a DataFrame, such as count, mean, and standard deviation.

  c. Matplotlib:

Purpose: Matplotlib is a plotting library for creating static, and animated visualizations in Python.

matplotlib.pyplot.plot(): This function is used to create line plots.

matplotlib.pyplot.xlabel(): It labels the x-axis of a plot, adding context to the data visualization.

2. Research an API. What is something unique about it that you learned in the documentation? What type of an API is it? What does it do? Brainstorm a potential scenario.

WeatherDataAPI

Unique Feature: The WeatherDataAPI provides real-time weather data and forecasts along with analysis of weather-related social media posts.

Type of API: The WeatherDataAPI is a RESTful API, which means it follows the principles of Representational State Transfer.

What it Does: The WeatherDataAPI offers weather information (current conditions, forecasts, historical data) for any location on the globe. It also provides sentiment scores (positive, negative, neutral) for weather-related keywords in social media posts and comments.

Scenario: Let's say you're developing a travel app, and you want to enhance the user experience by offering weather information AND an insight into how travelers are perceiving the weather at their intended destinations. You could use the WeatherDataAPI to fetch weather conditions and help others make travel decisions.

3. Import a data manipulation library and use a prefixed function and prefixed variable (w/comments)
import pandas as pd

# Prefixed function: pd.read_csv()

# This function reads data from a CSV file and returns it as a DataFrame.

data_frame = pd.read_csv('data.csv')
# Prefixed variable: pd.Series

# pd.Series is a one-dimensional array-like object that can hold any data type.

# It's often used to represent a single column of data within a DataFrame.

column_data = data_frame['column_name']