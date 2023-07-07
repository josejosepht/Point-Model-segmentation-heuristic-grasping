# Point-Model-segmentation-heuristic-grasping
The code repository implements PointNet, a deep learning model for point cloud analysis, specifically focusing on point cloud segmentation and heuristic grasping using segmentation output. The repository contains the following components:

PointNet Implementation: The repository includes the implementation of PointNet, which consists of the TNet module for the transformation network and the PointNetBackbone module for the backbone operations of PointNet. ReLU activations are applied between linear operations in the MLPs.



PointNet for Segmentation: The PointNetSeg module is implemented for point cloud segmentation. The module broadcasts the global feature vector to all point-wise features and performs additional point-wise processing. The compute_losses method applies cross entropy loss and regularization loss to improve class score predictions and ensure orthogonality of learned transformation matrices. The input point cloud is centered and normalized to enhance generalization.

![image](https://github.com/josejosepht/Point-Model-segmentation-heuristic-grasping/assets/97187460/bbd9ac75-30b3-4b4d-976b-6ce54fc368d3)



Heuristic Grasping using Segmentation Output: The code includes a heuristic approach to generate grasp poses for a coffee mug handle. It applies a PCA-based method to estimate the grasp pose by making assumptions about the alignment of the handle with principal axes. The code provides visualizations of grasp predictions for both upright and sideways orientations of the mug.


Upright mug:

![image](https://github.com/josejosepht/Point-Model-segmentation-heuristic-grasping/assets/97187460/cc1cc796-2819-4b47-9cc6-c3d7d92a75d0)


Non-upright mug:

![image](https://github.com/josejosepht/Point-Model-segmentation-heuristic-grasping/assets/97187460/cad79500-986e-4be4-a08e-7bdac029aa8d)
