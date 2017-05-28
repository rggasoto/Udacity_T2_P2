# Unscented Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program

This project implements a Unscented Kalman Filter using the bicicle model for tracking.
In order to properly model the process noise parameters, the NIS projection was used, resulting in final sigmas as 0.5 and 0.8 for laser and radar, respectivelly.


[//]: # (Image References)
[image1]: ./output_images/track.png

## 1-  Compiling

### Important Dependencies

* cmake >= v3.5
* make >= v4.1
* gcc/g++ >= v5.4

### Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./UnscentedKF path/to/input.txt path/to/output.txt`. You can find
   some sample inputs in 'data/'.
    - eg. `./UnscentedKF ../data/obj_pose-laser-radar-synthetic-input.txt`
## 2- Accuracy

The project was tested over provided data in `../data/obj_pose-laser-radar-synthetic-input.txt`

According to the criteria:


|Value |Minimum |Obtained |
|:---:|:---:|:---:|
|px |0.09 |0.06 |
|py |0.10 |0.08 |
|vx |0.40 |0.29 |
|vy |0.30 |0.20 |

Here we can see the result of the tracking:

![alt text][image1]

## 3- Follows the Correct Algorithm

The code was structured based on the previous project on EKF, therefore the algorithm was only updated to include the bicicle model and ukf augmented states and sigma points, according to the provided in lecture.

## 4- Code Efficiency

Where possible, the code was optimized to avoid excess multiplications or weird loops. There also should not have memory leaks or uncaught weird behavior.

