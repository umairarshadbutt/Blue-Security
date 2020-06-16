In this project you can find implementation of deep neural network for **people identification from video** by the characteristic of their **gait**. The processing is very robust against various covariate factors such as clothing, carrying conditions, shoe types and so on.

# Requirements
## Software Requirements
    • TensorFlow 1.8
    • Cuda 9.0
    • CuDNN 7.0
    • numpy, scipy, PIL
    • python 3.5.2
    • Tknr
## Hardware Requirements
    • RAM 4GB
    • GPU 11GB
    • Architecture x64
    • IP camera
    • WebCam
    
   
# Basic information about architecture
The network takes raw RGB video frames of a pedestrian as an input and produces one-dimensional vector - **gait descriptor** that exposes as an identification vector. The identification vectors from gaits of each two different people should be **linearly separable**. Whole network consists of two sub-networks connected in cascade – HumanPoseNN and GaitNN.
**Spatial features** from the video frames are extracted according to the descriptors that involve **pose of the pedestrian**. These descriptors are generated from the first sub-network - HumanPoseNN defined in human_pose_nn module. HumanPoseNN can be also used as a standalone network for regular **2D pose estimation problem** from still images.
Responsibility of the second sub-network - GaitNN defined in gait_nn module is the further processing of the generated spatial features into one-dimensional **pose descriptors** with the use of a residual convolutional network. Temporal features are then extracted across these pose descriptors with the use of the multilayer recurrent cells - **LSTM** or **GRU**. All temporal features are finally aggregated with **Average temporal pooling** into one-dimensional **identification vector** with good discriminatory properties. As already mentioned in the text above, the human identification vectors are linearly separable with each other and can therefore be classified with e.g. **linear SVM**.


## Author

👤 **Umair Arshad**

- Github: [@umairarshadbutt](https://github.com/umairarshadbutt)
- Twitter: [@its_UmairArshad](https://twitter.com/its_UmairArshad)
- Linkedin: [umair-arshad-butt](https://www.linkedin.com/in/umair-arshad-butt/)

👤 **Junaid Hussain**

- Linkedin: [unaid-hocane-muzamal](https://www.linkedin.com/in/junaid-hocane-muzamal/)

👤 **Muhi O Deen**

- Facebook: [@muhi.u.din](https://web.facebook.com/muhi.u.din)


