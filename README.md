# WiFi sensing experiment
Get to know about channel state information (CSI). [In wireless communications, channel state information (CSI) refers to known channel properties of a communication link. This information describes how a signal propagates from the transmitter to the receiver.](https://en.wikipedia.org/wiki/Channel_state_information) So, it can change raplidly as the wifi transmitter moves. Based on this characteristic, the CSI can be taken as the location fingerprint.

## Experiment Conponents
### A. Raw CSI data (10 points)
In this experiment, you will learn the constitution of CSI, including the Wi-Fi bandwidth, center frequency, the frequency of subcarriers, and so on. The data is stored in a h5 file. It can help you get to know more about CSI.
##### 1. Read the CSI data (2 points)
You need to load the given data set, and see what indicators are collected, and what is the meaning of each indicator.
##### 2. Combine CSI data (3 points)
The CSI data contains two parts, which are real part and imaginary part. You need to combine them.
##### 3. Visualize CSI data (5 points)
You need to visualize the CSI data, including the amplitude and phase.

### B. TRRS calculation (20 points)
As mentioned above, the CSI can be used as location fingerprint. In this part, you will learn how to obtain the fingerprint, which is called TRRS (time reversal focusing effect).
##### 1. Calculate TRRS from the dataset in the first part (10 points)
##### 2. Calculate the TRRS value matrix of a static location (10 points)
You need to calculate the TRRS value matrix of a static location, and visualize it.

### C. Cloest location (20 points)
The TRRS function can be used to track moving robot. We will give you a dataset, which contains the robot moving trajectory, along with the position labels, and the corresponding CSI data. And our question is: can we use TRRS to find the closest position of a given location.
##### 1. Visualize the robot moving trajectory (5 points)
The robot moving trajectory, and the positions of routers are given. You need to visualize them.
##### 2. Find the closest location (10 points)
Can we use TRRS to find the closest position of a given location. Calculate the TRRS of one (query) location X against all others, find the one that produces the max TRRS and pick it as the correct location, denoted as X'; Calculate the location distance (X, X'). Do this for some locations/samples in the dataset and produce the CDF plot. (It should be noticed that the CSI data in the given dataset is not good enough, so the CDF result may not be good.)
##### 3. Calculate the moving speed (5 points)
With the given location labels and timestamps, you can calculate the moving speed of the robot.

### D. RF-based inertial measurement (30 points)
In this section, we will turn a commodity WiFi device into an Inertial Measurement Unit (IMU) that can accurately track moving distance, heading direction, and rotating angle, requiring no additional infrastructure.
##### 1. Data presentation and preparation (0 points)
##### 2. Functions of RF-based inertial measurement (10 points)
You need to fill in the functions of RF-based inertial measurement according to the given formulas and related paper.
##### 3. Calculate the antenna alignment matrix (10 points)
Based on the functions, you need to calculate the antenna alignment matrix, which can tell the relative position between two antennas.
##### 4. Position Detection (10 points)
With the alignment matrix, you can know the relative position of these transmitters.

**The above four experiments are fundamental and must be done by all of you. If you are not able to handle the extend experiment, which is the fourth part, it's OK to just finish four of them. And you will get almost 80 points if you do a good job.**

### E. Extend experiment (10 points)
In the third part, you can find that it is unstable to track the closest position (relocalize) by using TRRS only. To improve the performance, you can try to use the CSI data collected from other antennas or even other APs. You are also encouraged to use some state-of-the-art methodologies to handle the CSI information, such as machine learning, or deep learning. And then we can judge how much further your algorithm can achieve. It should be noticed that this part will be graded in terms of experimental completness and accuracy, as well as the cross-sectional comparison with other groups.
The refereced dataset link is: https://www.kaggle.com/competitions/wild-v2/overview, which consists of the training datasets and the test datasets.

***Let's start our trip with CSI***

### File Declaration

WiFi sensing.pdf: basic knowledge of wifi sensing, espcially the RF-based inertial measurement

TRRS release.pdf: an example of output results of jupyter notebook

TRRS release.ipynb: the given code and the experiment requirement

### P.S.

Due to the limitation of time, the materials and documents of the experiment may be insufficient, your comments are welcome.