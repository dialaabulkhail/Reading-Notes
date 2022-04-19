**Mark what you didn't need in your project as (was not used)**

## Artifical intillegence
To make computers think like humans.
Machine learning (ML) and deep learning (DL) are also approaches to solving problems. The difference between these techniques and a Python script is that ML and DL use training data instead of hard-coded rules, but all of them can be used to solve problems using AI

## Deep learning
Deep learning is a technique in which you let the neural network figure out by itself which features are important instead of applying feature engineering techniques. This means that, with deep learning, you can bypass the feature engineering process.

## Feature engineering
Used to train a model to predict the sentiment in a sentence? Or what if you have an image, and you want to know whether it depicts a cat?

Another name for input data is feature, and feature engineering is the process of extracting features from raw data.
- Not having to deal with feature engineering is good because the process gets harder as the datasets become more complex.

## Neaural networks
It is a system that learns to predict output by:
1. taking input data
2. make a prediction
3. compare it to expected output
4. adjust internal state to predict correctly.

Vectors, layers, and linear regression are some of the building blocks of neural networks. The data is stored as vectors, and with Python you store these vectors in arrays.

Each layer transforms the data that came from the previous layer by applying some mathematical operations.

```
python -m pip install ipython numpy matplotlib

ipython
```

[AI, Neural network, Deep learning, Feature engineering](https://realpython.com/python-ai-neural-network/)
_____

## TensorFlow
Tenserflow is a library used to build neural networks, its used for machine learning applications easily with an API called Keras.
tensorflow was mainly used for detecting ard recognising (like traffic lights/pedestrian).
 - Applications of Tensorflow:
1. Analyzing rush-hour (peak) traffic
2. Predicting car accident risk
3. Greater knowledge of on-road conditions - like weather change
4. Driving behavior over specific roads-  for example, it uses Flow/Density models to calculate relative speeds
5. The effectiveness of safety measures

[Road safety-Tensorflow](https://www.datasciencecentral.com/how-tensorflow-is-helping-in-maintaining-road-safety/)

- Keras is used as a high-level API to build and train models in TensorFlow.  [Modules](https://www.tensorflow.org/api_docs/python/tf/keras)

[Quick start Keras](https://www.tensorflow.org/tutorials/keras/classification)

[Quick start](https://www.tensorflow.org/tutorials/quickstart/beginner)
_____

## API
API stands for application programming interface, which is a set of definitions and protocols for building and integrating application software.

This interface allows different systems to talk to each other without having to understand exactly what each other does.

- SOAP vs REST vs GraphQL
1. SOAP (Simple Object Access Protocol) is typically associated with the enterprise world, has a stricter contract-based usage, and is mostly designed around actions.
2. REST (Representational State Transfer) is typically used for public APIs and is ideal for fetching data from the web. It’s much lighter and closer to the HTTP specification than SOAP.
3. GraphQL. Created by Facebook, GraphQL is a very flexible query language for APIs, where the clients decide exactly what they want to fetch from the server instead of the server deciding what to send.

When consuming APIs with Python, there’s only one library you need: requests.

> import requests

> requests.get("https://randomuser.me/api/")

[API's](https://realpython.com/python-api/)
____
## Pygame
python library used for making multimedia applications like games, art, music, sound, video and multimedia projects. 

[Official webpage](https://www.pygame.org/news)

[Tutorial](https://realpython.com/pygame-a-primer/)
____
## Simpy
Python framework for event simulation. 

SimPy is a process-based discrete-event simulation framework based on standard Python.

Processes in SimPy are defined by Python generator functions and may, for example, be used to model active components like customers, vehicles or agents. SimPy also provides various types of shared resources to model limited capacity congestion points (like servers, checkout counters and tunnels).
[SimPy](https://simpy.readthedocs.io/en/latest/)

[Tutorial](https://realpython.com/simpy-simulating-with-python/)
_____
