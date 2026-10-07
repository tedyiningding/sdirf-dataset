---
layout: default  # Or another layout if you have one
title: Sensor Setup
permalink: /sensor_setup/ 
---
<style>
.wrapper { max-width: 1200px; padding-left: 24px; padding-right: 24px; }
</style>

# Camera
We used an off-the-shelf [ZED 2i Stereo Camera](https://www.stereolabs.com/en-gb/store/products/zed-2i) (lens focal length 2.1 mm, no polariser), which has a built-in IMU and magnetometer.

# On-road data collection setup
<center>
    <img src="{{ site.baseurl }}/assets/on_road_data_collection_setup.png" width="500">
</center>


<div style="margin-top: 24px;"></div>

The camera was placed behind the windshield of a car and connected to a laptop installed with the [ZED software development kit (SDK)](https://www.stereolabs.com/en-gb/developers/release) (v4.0.6) and the [ZED Robot Operating System (ROS) wrapper]((https://github.com/stereolabs/zed-ros-wrapper)) (v4.0.5).
Considering the way the windshield inclines and that the mounting holes are located at the bottom of the camera but not at its top, it was mounted upside down for convenience and safety reasons.

We accordingly set the `camera_flip` parameter to `true` to allow the SDK to account for this upside-down setup to generate the correct stereo images.
The left frames of these images, whose poses are estimated by a SLAM algorithm in our method and to which the 3D positions of all landmarks are referenced, were actually acquired by the right camera because of this upside-down setup.
Therefore, our [photometric calibration]({{ site.baseurl }}/photometric_calibration/) was later performed on the right camera.

We disabled the camera’s auto-white balance and auto-exposure functionalities.
Instead, we used a fixed white balance, and manually adjusted the exposure time, in conjunction with the gain, according to the lighting condition of the scene.
We took note of the combination of exposure time and gain used to collect each data sequence (eight different combinations in total).
Later we performed a photometric calibration for each combination of these two parameters.

Additionally, a number of parameters which control various image processing algorithms applied to the RAW images by the onboard image signal processor are
also configurable.
We fixed these parameters throughout our on-road data collection and photometric calibration.
The following table shows a full list of camera settings we used.
For the description and the valid value range for some of the settings, please refer to the [StereoLabs Docs](https://www.stereolabs.com/docs/video/camera-controls).

<center>
<table border="1" cellspacing="0" cellpadding="6" style="border-collapse:collapse; text-align:center;">
    <style>
        th {
            text-align: center;
        }
    </style>

  <!-- <caption style="font-weight:bold; margin-bottom:8px;">
    TABLE I<br>
    THE CAMERA SETTINGS
  </caption> -->

  <thead>
    <tr>
      <th rowspan="2">Setting</th>
      <th colspan="2">Value/Configuration</th>
    </tr>
    <tr>
      <th>On-road data collection</th>
      <th>Photometric calibration</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Camera flip</td>
      <td>True</td>
      <td>False</td>
    </tr>
    <tr>
      <td>Resolution</td>
      <td colspan="2">1920 × 1080</td>
    </tr>
    <tr>
      <td>Frame rate</td>
      <td>15 Hz</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td>White balance</td>
      <td colspan="2">4700</td>
    </tr>
    <tr>
      <td>Gain</td>
      <td rowspan="2">Sequence dependent</td>
      <td rowspan="2">Same as the on-road data collection</td>
    </tr>
    <tr>
      <td>Exposure</td>
    </tr>
    <tr>
      <td>Brightness</td>
      <td colspan="2">4</td>
    </tr>
    <tr>
      <td>Contrast</td>
      <td colspan="2">4</td>
    </tr>
    <tr>
      <td>Hue</td>
      <td colspan="2">0</td>
    </tr>
    <tr>
      <td>Saturation</td>
      <td colspan="2">4</td>
    </tr>
    <tr>
      <td>Sharpness</td>
      <td colspan="2">4</td>
    </tr>
    <tr>
      <td>Gamma</td>
      <td colspan="2">5</td>
    </tr>
    <tr>
      <td>Image enhancement</td>
      <td colspan="2">Disabled</td>
    </tr>
  </tbody>
</table>
</center>

# Data format
During the collection, the data, together with the timestamps, was logged to ROS bags, which were later parsed to generate the following files (see the [Overview]() page for the folder structure).
- Rectified left and right images at a frame rate of 15 Hz saved as PNG files, each at a resolution of 1920×580.
- IMU data at a rate of 400 Hz saved as CSV files.
- Magnetometer data at a rate of 50 Hz saved as CSV files.

Note that
- The stereo rectification was performed by the ZED SDK using its factory calibrated stereo parameters.
<!-- - The stereo images have been processed by the camera’s onboard Image Signal Processor (ISP).
The RAW images are not available. -->
- The original image size was 1920×1080.
The images were later cropped by 290 pixels at the top (to remove the mostly-sky region) and by 210 pixels at the bottom (to remove the car’s bonnet and interior reflections caused by the windshield).
See the image below for an example image of the left frame before and after the cropping (outlined in red).
The final image size after cropping has an aspect ratio of 1920/580 ≈ 3.31, which is very close to the aspect ratio (1241/376 ≈ 3.30) of the images in the [KITTI odometry benchmark](https://www.cvlibs.net/datasets/kitti/eval_odometry.php).

<center>
    <img src="{{ site.baseurl }}/assets/example_image_before_and_after_cropping.png" width="800">
</center>


<div style="margin-top: 24px;"></div>

# Camera intrinsic parameters
The intrinsic parameters of the camera (after stereo rectification) are specified in our [GitHub repo](https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/Examples/Stereo/SDIRF.yaml).
Note that these parameters have already taken into account of the upside-down setup of our on-road data collection as well as our cropping, and therefore can be directly used for the images in SDIRF.