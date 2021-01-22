# VehicleModel
This repository contains code and associated files for Vehicle modeling using basic calculus, matrix manipulation and Python libraries. This repository consists of a number of tutorial notebooks for various coding exercises, labs and mini-project files.

## Table Of Contents

### Tutorials
* [KeepTrack_lab1](/KeepTrack_lab1) 
    * Plotting Position vs Time: plots a position vs time graph of the data
    * Approaching Instantaneous Speed
    * Speed from Position Data: differentiates (taking the derivative of) displacement data.
    * Implement an Accelerometer
    * Understanding the Derivative: Position, velocity, and acceleration are all useful quantities when describing a vehicle's motion and these quantities are related through the derivative.

* [KeepTrack_lab2](/KeepTrack_lab2)
    * Plotting Elevator Acceleration: direct access to the phone's IMU data, including data from the accelerometers, rate gyros, and magnetometer and plots acceration while taking an elevator
    * Approximating the Integral : plots "Area Under a Curve" where horizontal axis is in units of seconds and the vertical axis is in units of meters / second.
    * Integrating Accelerometer Data : uses the integral to go from acceleration data to position data and accumulates change by calculating the area of lots of little rectangles and summing them up
    * Integrating Rate Gyro Data
    * Accumulating Errors: visualizes accumulating errors has a bigger impact on integrated data when we give that data time to accumulate.
 
* [KeepTrack_lab3](/KeepTrack_lab0): plots keeping track of a vehicle's x and y coordinates as it moves in any direction


### Mini-Project: Trajectory_lab
[Trajectory_lab](/Trajectories_lab/Reconstructing%20Trajectories.ipynb) is a notebook and collection of Python files. This project about with reading sensor data from a self-driving car and determining the car's trajectory and path over time using calculus. The raw sensor data looks like this: 
* timestamp - Timestamps are all measured in seconds. The time between successive timestamps (Δt) will always be the same within a trajectory's data set (but not between data sets).
* displacement - Displacement data from the odometer is in meters and gives the total distance traveled up to this point.
* yaw_rate - Yaw rate is measured in radians per second with the convention that positive yaw corresponds to counter-clockwise rotation.
* acceleration - Acceleration is measured in 𝑚/𝑠^2 and is always in the direction of motion of the vehicle (forward).

This raw sensor data is saved in a file called trajectory_example.pickle loaded using a helper function. The main fuction of this notebook provides:
* get_speeds - returns a length 𝑁 list where entry 𝑖 contains the speed (𝑚/𝑠) of the vehicle at 𝑡=𝑖×Δ𝑡 
* get_headings - returns a length 𝑁 list where entry 𝑖 contains the heading (radians, 0≤𝜃<2𝜋) of the vehicle at 𝑡=𝑖×Δ𝑡
* get_x_y - returns a length 𝑁 list where entry 𝑖 contains an (x, y) tuple corresponding to the 𝑥 and 𝑦 coordinates (meters) of the vehicle at 𝑡=𝑖×Δ𝑡
* show_x_y - generates an x vs. y scatter plot of vehicle positions.
all of which take a processed data_list (with 𝑁 entries, each Δ𝑡  apart) as input
