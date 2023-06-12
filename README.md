# turtlebot3_autorace_2023
- ROBOTIS [turtlebot3_simulations](https://github.com/ROBOTIS-GIT/turtlebot3_simulations) 사용 (해당 패키지 설치 필수)
- ROBOTIS [turtlebot3_autorace_2020](https://github.com/ROBOTIS-GIT/turtlebot3_autorace_2020) 응용

## export 항목
```
export AUTO_DT_CALIB=action
export AUTO_IN_CALIB=action
export AUTO_EX_CALIB=action
export GAZEBO_MODE=true
export TURTLEBOT3_MODEL=burger
```

## roslaunch 항목
```
$ roslaunch turtlebot3_autorace_core turtlebot3_autorace_2023.launch
$ roslaunch turtlebot3_autorace_core turtlebot3_autorace_core.launch
$ roslaunch turtlebot3_autorace_camera intrinsic_camera_calibration.launch
$ roslaunch turtlebot3_autorace_camera extrinsic_camera_calibration.launch
$ roslaunch turtlebot3_autorace_dectect detect_modified.launch
$ roslaunch turtlebot3_autorace_driving turtlebot3_autorace_control_lane.launch
```

## 기존 turtlebot3_autorace_2023과의 변경사항
 - turtlebot3_autorace_camera 노드의 image_compensation 의 0 나누기 에러 해결
 - turtlebot3_autorace_driving 노드의 control_lane 을 응용한 control_modified 제어기법 사용
 - lane detection의 집중을 위한 turtlebot3_gazebo의 autorace2020 맵을 수정
