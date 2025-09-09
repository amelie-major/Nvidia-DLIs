# Building Real-Time Video AI Applications

There so many usecases for real-time video AI applications, including:

* Access Control
* Traffic Engineering
* Parking management
* Content Engineering

These demand robust real-time video applications, and these tend to be deep learning neural network models trained from a specific task. These tasks may involve:

* Classification - identifying the type of object in frame
* Localisation - using regression to find the coordinates of object in the frame
* Segementation

The AI inference can occur on premise, in the cloud or on the edge. We pass the insights downstream for more analysis. When inference is performed on the edge, allowing for faster response time and lower bandwidth cost. 
> You need to create a data processing pipeline that optimize efficiency and accuracy. 

They require the versatility to deploy on different devices. 

## DeepStream Open SDK

This is a open-source multi-media analytics framework that uses plugins to construct the pipeline. There are three key concepts:

* Elements - these are the core building blocks, processing from source to sink, passing through filter elements, such as source item passing element to stream and custom elements
* Pads - used to negotiate between elements
* Plugins - basic building blocks connected through pads
* Bins - a container for collection of plugins
* Pipeline - top level bin providing a bus and managing synchronization

## Streaming data

Provides several mechanism for communication and data exchange between application and pipeline

* Buffers - pass streaming data between plugins in the pipeline
* Events - sends info between plugins or from the application to the plugin
* Messages - posts info on message bus for collection by the application
* Queries - allow applications to request information from the pipeline

*Probe* is implemented as callback function that can be attached to a pad and interact with data flowing through the pipeline.

## How can we measure performance within the pipeline?

* Accuracy - this can include intersection over union and mean-average precision
* Throughput - the quantity of data being sent and recieved within a unit of time
* Latency - the time taken to be transferred across the network
* Hardware utilization

