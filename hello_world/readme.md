# TensorflowJS / Hello_World
* A project which shows a simple Hello World app, using Tensorflow JS.
* Adapted from the example provided [here](https://js.tensorflow.org/#getting-started).

# Setup
* Clone the [repo](https://github.com/jailad/tensorflowjs).
* Open up hello_world/index.html in a browser of your choice.
* No additional setup required !

# Code Walkthrough

## Source TensorflowJS Script
    > '<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@0.6.1"></script>'

## Define the (shallow) network
    > const model = tf.sequential();
    > model.add(tf.layers.dense({ units: 1, inputShape: [1] }));
    > model.compile({ loss: 'meanSquaredError', optimizer: 'adam' });

## Define the training data set
* xs = inputs, ys = outputs
    > const xs = tf.tensor2d([1, 8, 7, 9, 10], [5, 1]);
    > const ys = tf.tensor2d([1, 12, 13, 15, 17], [5, 1]);

## Train the model
* We will set the batch size as 2, and train for 30 epochs.
    > model.fit(xs, ys, { batchSize: 2, epochs: 30})

## Generate predictions from the model
* Once we have a trained model, we can generate predictions from the same.
    > model.predict(tf.tensor2d([5], [1, 1])


# Output
[output]: images/output.png "Output"
![alt text][output]
