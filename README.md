# Point-Model-segmentation-heuristic-grasping
The code repository implements PointNet, a deep learning model for point cloud analysis, specifically focusing on point cloud segmentation and heuristic grasping using segmentation output. The repository contains the following components:

PointNet Implementation: The repository includes the implementation of PointNet, which consists of the TNet module for the transformation network and the PointNetBackbone module for the backbone operations of PointNet. ReLU activations are applied between linear operations in the MLPs.

PointNet for Segmentation: The PointNetSeg module is implemented for point cloud segmentation. The module broadcasts the global feature vector to all point-wise features and performs additional point-wise processing. The compute_losses method applies cross entropy loss and regularization loss to improve class score predictions and ensure orthogonality of learned transformation matrices. The input point cloud is centered and normalized to enhance generalization.

Heuristic Grasping using Segmentation Output: The code includes a heuristic approach to generate grasp poses for a coffee mug handle. It applies a PCA-based method to estimate the grasp pose by making assumptions about the alignment of the handle with principal axes. The code provides visualizations of grasp predictions for both upright and sideways orientations of the mug.
