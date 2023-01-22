# Early Fusion
Projection lidar point clouds image and fusing it with 2D object detection bounding boxes


### Input Point Cloud
<p align="center">
<img src="https://github.com/varshasathya/Early_Fusion/blob/main/pcd_op.PNG" width=640>
</p>

### 2D object detection using YOLO-v4
<p align="center">
<img src="https://github.com/varshasathya/Early_Fusion/blob/main/out4_yolo_small.gif" width=640/>
</p>

### 3D Lidar Points Projected on the image plane
<p align="center">
<img src="https://github.com/varshasathya/Early_Fusion/blob/main/out_video2.avi" width=640/>
</p>

### LiDAR points Fused with YOLO detections
<p align="center">
<img src="https://github.com/varshasathya/Early_Fusion/blob/main/fusion_ouput.mp4" width=640/>
</p>

<p align="center">
    1. LiDAR points are projected on the image using camera instrinsic and extrinsic matrix <br />
    2. The points that lie within the detected 2D Bounding Box by YOLO are stored and rest are ignored <br />
    3. There are some outliers inside bboxes that do not belong to that category, to reject these outliers there are several ways. <br />
    4. One way is to shrink the bounding box size so that the points that absolutely belong to the desired objects are only considered. <br />
    5. Another way is to use the Sigma Rule, i.e include the points that are within 1 sigma or 2 sigma away from gaussian mean, based on the distance of points <br />
</p>

