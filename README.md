# Sine-Model-DL
A NN to model sine func.
Summary of the first four chapters of the TinyML book

The goal of this book is to show how we can build our projects running machine learning (ML) on embedded devices. 

The first chapter explains where the idea of TinyML comes in.

The second chapter introduces all the software and the hardware development kits required to do the projects. For most projects, machine learning models are trained in the cloud, using Google Colab environment and then an embedded development board is required to test the programs on. For this purpose, three boards including SparkFun Edge board, Arduino Nano 33 BLE Sense and STM32F746G Discovery kit are recommended. All of the projects in this book are based around the TensorFlow Lite for Microcontrollers framework. 

The third chapter explains the basic workflow for creating and using a deep learning Model to predict when a factory machine is likely to break down, after training model and evaluating it, TensorFlow Lite interpreter is introduced to run models on small, low powered devices. After the model has been converted, the TensorFlow Lite for Microcontrollers C++ library is utilized to load the model and make predictions.

In the fourth chapter, the goal is to train a model that can take a value, x, and predict its sine. To create the model, Python, TensorFlow, and Google’s Colaboratory are used. For this purpose, the following steps are done.
1-	Importing dependencies including TensorFlow, Numpy, Matplotlib.pylab and math.
2-	Generating a uniformly distributed set of random numbers in the range from 0 to 2π, shuffling them, calculating the corresponding sine values and adding a small random noise to them
3-	Splitting data into three parts including training, validation and test data.
4-	Using Keras to create a simple model architecture. The first layer has a single input and 16 neurons. It’s a fully connected layer. Each neuron will then become activated to a certain degree using ReLU. 
5-	Training the model using MSE loss function and evaluating the performance of it
6-	Improving the performance of the model by adding another layer of neurons
7-	Using TensorFlow Lite converter to convert TensorFlow models into two new versions of the model. The first is converted to the TensorFlow Lite FlatBuffer format, but without any optimizations. The second is quantized.
8-	Making predictions with TensorFlow Lite as follows:
•	Instantiate an Interpreter object.
•	Call some methods that allocate memory for the model.
•	Write the input to the input tensor.
•	Invoke the model.
•	Read the output from the output tensor.
9- Converting the model into a C source file that can be included in the application

These chapters were the first taste of using Keras to train a tiny model.

