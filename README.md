Automatic Ground Truth Generation in CARLA 
=============================================

This Python API gets a variety of data from CARLA Simulator and also helps automatically generate Ground Truth according to the Darknet YOLO Framework.

<img src="https://user-images.githubusercontent.com/36737287/82050024-5c1edd00-96f2-11ea-810d-3f8fcc664901.png" width="90%">

Installation
--------------
> cd [carla directory]/PythonAPI/examples  
> git clone https://github.com/JangJaeSung/carla_ground_truth.git

generate_ground_truth.py
---------------------------
This API helps you information about the RGB Image, Semantic Segmentation Image and Bounding Box of Objects from the CARLA Server. In addition, it allows users to capture these informations at regular intervals and keyboard input.

CARLA Server on  
> ./CarlaUE4.sh

Spawn Object and Change Various Weathers (CARLA Python example) Link: [https://github.com/carla-simulator/carla/tree/master/PythonAPI/examples]
> ./spawn_npc.py  
> ./dynamic_weather.py  

Execute Generating Code  
> ./generate_ground_truth.py -l N  

object_bounding_box.py
------------------------
This API helps to post-process the data obtained above and to create a Ground Truth for Darknet YOLO Framework.  
Data for learning is stored in folder 'custom_data', and the results of the bounding box generated in folder 'draw_bounding_box' can be seen.
> ./object_bounding_box.py  


