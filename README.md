# TensorFlow Lite Coin Detection Android Demo

This code sample is a forked from [Tensorflow Lite Object Detection Demo](https://github.com/tensorflow/examples/tree/master/lite/examples/object_detection/android).

### Overview
This is a camera app that continuously detects the coins (bounding boxes and classes) in the frames seen by your device's back camera,
using a [custom model](https://storage.googleapis.com/coin-saved-model/tflite/coin-detector-tflite.zip) model trained Google AutoML Vision.

The model files are downloaded via Gradle scripts when you build and run. You don't need to do any steps to download TFLite models into the project explicitly.


## Build the demo using Android Studio

### Prerequisites

* If you don't have already, install **[Android Studio](https://developer.android.com/studio/index.html)**, following the instructions on the website.

* You need an Android device and Android development environment with minimum API 21.
* Android Studio 3.2 or later.

### Building
* Open Android Studio, and from the Welcome screen, select Open an existing Android Studio project.

* From the Open File or Project window that appears, navigate to and select the tensorflow-lite/examples/object_detection/android directory from wherever you cloned the TensorFlow Lite sample GitHub repo. Click OK.

* If it asks you to do a Gradle Sync, click OK.

* You may also need to install various platforms and tools, if you get errors like "Failed to find target with hash string 'android-21'" and similar.
Click the Run button (the green arrow) or select Run > Run 'android' from the top menu. You may need to rebuild the project using Build > Rebuild Project.

* If it asks you to use Instant Run, click Proceed Without Instant Run.

* Also, you need to have an Android device plugged in with developer options enabled at this point. See **[here](https://developer.android.com/studio/run/device)** for more details on setting up developer devices.


### Model used

The model is created from a custom datasets of coins photo. Currently only use Indonesian Rupiahs and Japanese Yen.
Downloading, extraction and placing it in assets folder has been managed automatically by download.gradle.

If you explicitly want to download the model, you can download from **[here](https://storage.googleapis.com/coin-saved-model/tflite/coin-detector-tflite.zip)**. Extract the zip to get the .tflite and label file.