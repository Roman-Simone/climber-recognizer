<div align="center">
  <h1 style="border-bottom: none;">Climber Recognizer</h1>
  <img src="https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54" alt="Python"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/Numpy-013243?style=flat&logo=numpy&logoColor=white" alt="NumPy"/>
</div>


## Table of contents

-   [Description](#Description)
-   [Project Structure](#project-structure)
-   [Installation](#Installation)
-   [Running the project](#Running-the-project)

## Description
This project has two goals:
- The first is to create software capable of recognizing an indoor climbing route given a photo and the color of the route holds
- The second to perform tracking of a climber using a video as input. Two modes were used the first is with optical flow while the second is with background subtractor

To simulate this, a graphical user interface was created with python's tkinter library.
> [!WARNING]
> This part of GUI works properly with python 3.10 with other python versions there may be problems with tkinter library.

For more information, please refer to the [Report_project](https://github.com/Roman-Simone/Climber_recognizer/blob/main/Report_project.pdf) document. 

#### Results recognize climbing route

<div align="center">
   <img src="Media/img_lead_2_crop.jpg" style="width: 10%; margin-right: 20px; text-align: center">
   <img src="Media/img_lead_2_crop_processed.jpg" style="width: 10%;">
</div>


#### Results tracking climber


<div align="center">
    <img src="Media/video_climber_processed.gif" style="width: 50%;">
</div>


## Project Structure
```BASH
├── Media
│   ├── img_lead_1.jpg
│   ├── img_lead_1_crop.jpg
│   ├── img_lead_2.jpg
│   ├── img_lead_2_crop.jpg
│   ├── img_lead_2_crop_processed.jpg
│   ├── video_climber.mp4
│   └── video_climber_processed.gif
├── README.md
├── Report_project.pdf
├── Script
│   ├── FindClimbingRoute
│   │   ├── FindClimbingRoute.py
│   │   ├── FindClimbingRouteDemo.py
│   │   └── utils.py
│   ├── TrackingClimber
│   │   └── TrackingClimber.py
│   └── main.py
└── requirements.txt
```
## Installation

In order to run the project you'll need to clone it and install the requirements. I suggest you to create a virtual environment. These are the steps:
- Clone it

    ```BASH
    git clone https://github.com/Roman-Simone/CLIMBER_RECOGNIZER.git
    ```
- Create the virtual environment 
  
    ```BASH
    python -m venv name_of_virtual_env
    ```
- Activate the virtual environment
    ```BASH
    source name_of_virtual_env/bin/activate
    ```
- Install the requirements
    ```BASH
    pip install -r requirements.txt
    ```

## Running the project

The project can be runned in two different ways:
- through the GUI:
     
  
    ```
    python main.py     
    ```
    
    After running it a menu will be opened and there select the demo you want to try out.
> [!WARNING]
> This part works properly with python 3.10 with other python versions there may be problems with tkinter library. You can still directly run scripts where tkinter is not used.
    

- Running directly:
        
     - To run the Tracking Climber part:
     
        ```
        python TrackingClimber.py
        ```
        
        if you want to change the tracking modes change the variable method:
        
        ```
        method = "BackgroundSubtractorKNN"
        or
        method = "OpticalFlow"
        ```
     - To run the find route part demo:
       
        ```
        python FindClimbingRouteDemo.py
        ```
             
     - To run the GUI of find route
     
        ```
        python FindClimbingRoute.py  
        ```
> [!WARNING]
> The last part of GUI works properly with python 3.10 with other python versions there may be problems with tkinter library.


# Contacts

Simone Roman - [simone.roman@studenti.unitn.it](mailto:simone.roman@studenti.unitn.it)

<a href="https://www.unitn.it/"><img src="https://ing-gest.disi.unitn.it/wp-content/uploads/2022/11/marchio_disi_bianco_vert_eng-1024x295.png" width="300px"></a>
