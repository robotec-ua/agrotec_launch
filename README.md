# Agrotec robot launch package
This is the package dedicated to start all the system of Robotec packages. All the parameters are stored here, so the packages doesn't need to be configurated.

## Table of contents
* [Project structure](#project_structure)
    * [Folders](#folders)
    * [Files](#files)
* [Usage](#usage)

## Project structure
```
.
├── launch
│   ├── agrotec_launch
│   │   └── agrotec_launch.launch
│   ├── move_basic
│   │   └── move_basic.launch
│   ├── pid
│   ├── robotec_mrcnn
│   │   └── robotec_mrcnn.launch
│   ├── robotec_odom_publisher
│   │   └── robotec_odom_publisher.launch
│   ├── robot_localization
│   │   └── robot_localization.launch
│   ├── robot_pose_publisher
│   │   └── robot_pose_publisher.launch
│   ├── rosserial_python
│   │   └── rosserial_python.launch
│   └── tf2
│       └── tf2.launch
├── param
│   ├── imu
│   │   └── imu_calibration.yaml
│   ├── move_basic
│   │   └── move_basic.yaml
│   ├── robotec_mrcnn
│   │   └── robotec_mrcnn.yaml
│   └── robot_localization
│       └── robot_localization.yaml
├── CMakeLists.txt
├── LICENSE
├── package.xml
├── README.md
└── TODO.md
```

### Folders
* `include` : C/C++ Headers and ROS Messages/Services
* `msg` : ROS messages files
* `scripts` : miscellaneous scripts needed by the project 
* `srv` : ROS services files

### Files
* `CHANGELOG.md` : the file where the changes to the project are desribed
* `README.md` : the documentation of the project
* `TODO.md` : suggesting changes in the package 
* `launch/<package_name>/<package_name>.launch` : launching <package_name> with desired parameters
* `param/<package_name>/<package_name>.yaml` : desired parameters for <package_name>
* `imu_calibration.yaml` : calibration parameters for the IMU, used in Robotec products (MPU9250)

## Usage
Everything you need to start the whole robot is to run the command :
```bash
$ roslaunch agrotec_launch agrotec_launch/agrotec_launch.launch
```