# Writeup: Track 3D-Objects Over Time

Please use this starter template to answer the following questions:

### 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?
-filter: Kalman Filter is implemented as 'Filter' class. This class has methods for calculation of Kalman Filter parameters, state prediction and motion update. 
-track management: Track management is implemented as 'Trackmanagement' class. Depend on measurements and association, the track management add/delete track and change track score. a
-association: Association is implemented as 'Association' class. The unassigned tracks and unassigned measurements are associated. To associate the closest measurement and track, this class use the mahalanobis distance and gating. 
-camera fusion: To improve object detection, both LiDAR sensor and camera sensor data are used.

### 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)? 
update times are increased. Since different types of sensors are used, noise can be reduced on one side. In my results.

### 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?
The difference of visibility between LiDAR and camera cause uncertain track updates. In this project, I cannot see it in yaw direction. but, in x direction, camera sensor looks like not be able to measure too far point.

### 4. Can you think of ways to improve your tracking results in the future?
Visibility of camera should be extended. Therefore, cameras should be put on right and left sides. thats what big company like waymo do in real projects. 

