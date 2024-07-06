
# MSSD-SLAM-Dataset

This repository provides the MSSD-SLAM dataset, which includes dynamic scenes captured using the RealSense D455 camera. The dataset is designed to support the evaluation and development of SLAM algorithms in dynamic environments.

## Dataset Description

The dataset is provided in ROS bag format and includes the following information:
- **RGB Information**: Color images captured using the RealSense D455 camera.
- **Depth Information**: Depth images captured using the RealSense D455 camera.
- **IMU Data**: Inertial measurement unit data captured using the RealSense D455 camera.

## Download Links
The dataset can be downloaded from the following Baidu Yun links: 链接：https://pan.baidu.com/s/1cjr4PCf9BlPGd59mom8xzw 
提取码：63he

### Ground Truth

The ground truth data is provided in a separate `txt` file. It includes high-precision trajectories obtained from a motion capture system. Note that there is a time offset between the ground truth and the recorded dataset. Users should account for this offset when evaluating their algorithms.

### Time Offset Adjustment

When using the `evo` tool for evaluation, you can adjust for the time offset using the `--t_offset` parameter. The time offset is approximately 1.5 seconds, but we recommend users to fine-tune this value based on their specific requirements.

### Example Usage with `evo`

```sh
evo_ape tum ground_truth.txt trajectory.txt --t_offset 1.5

