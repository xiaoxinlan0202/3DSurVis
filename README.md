# 3D Object Detection for Autonomous Driving: A Comprehensive Survey (2015-2024)

This repository hosts a [SurVis](https://github.com/fabian-beck/survis)-based interactive literature survey visualizing the landscape of 3D object detection techniques specifically for autonomous driving, covering 10 research papers from 2015 to 2024. The survey delves into the evolution, current methodologies, and potential future trajectories of this critical perception component in autonomous vehicle systems.

## 📊 Overview

3D object detection is fundamental to the perception capabilities of autonomous vehicles. It enables the precise localization of surrounding objects (e.g., vehicles, pedestrians, cyclists, and other obstacles) in three-dimensional space. By achieving accurate detection, autonomous driving systems can make informed and safe navigation decisions, significantly contributing to enhanced road safety and operational efficiency.

This survey systematically analyzes research published in major computer vision conferences (CVPR, ICCV, ECCV) and influential arXiv preprints between 2015 and 2024. It tracks the evolution of the field through distinct phases:

* **2015-2017:** Initial exploration phase, characterized by foundational work and limited datasets.
* **2018:** A breakthrough year, marked by the introduction of the PointNet series and the verification of voxel-based CNNs.
* **2019-2021:** A period of accelerated development with a diversification of approaches and techniques.
* **2022-2024:** An integration phase, with a strong focus on Bird's-Eye View (BEV) Transformer models and end-to-end trainable systems.

## 🔍 Survey Scope

This survey concentrates on 3D object detection algorithms designed for **outdoor scenes** within the context of **autonomous driving**. The primary areas covered include:

* **LiDAR-based methods:** Techniques that primarily use Light Detection and Ranging data.
* **Camera-based methods:** Approaches relying on monocular, stereo, or multi-view camera systems.
* **Multi-modal fusion approaches:** Methods that combine data from multiple sensor types (e.g., LiDAR and camera).
* **Hybrid and graph-based techniques:** Innovative methods employing combinations of feature representations or graph neural networks.

The research examined predominantly focuses on **vehicle-mounted perception systems** designed to detect traffic participants and obstacles within a typical range of **10-150 meters** in complex urban environments. Performance is often evaluated using standard autonomous driving benchmarks such as **KITTI** and **nuScenes**.

## 📚 Literature Categories

The surveyed literature is organized into four main categories based on the primary input modality and processing architecture:

### 1. LiDAR-Based Methods
These methods leverage the rich 3D geometric information provided by LiDAR sensors.
* **VoxelNet:** An end-to-end learning framework that processes raw point clouds by dividing them into volumetric pixels (voxels) and applying 3D convolutions.
* **PointPillars:** An efficiency-focused approach that utilizes "pillars" (vertical columns of points) to create pseudo-images, enabling faster 2D convolutions for feature extraction and detection.
* **PointRCNN:** A two-stage detector that directly learns point-wise features from raw point clouds for proposal generation and refinement.

### 2. Camera-Based Methods
These approaches aim to perform 3D object detection using only image data, which is more cost-effective but inherently challenging due to the lack of direct depth information.
* **Pseudo-LiDAR:** A technique that first estimates depth from monocular or stereo images and then converts this depth map into a 3D point cloud representation, allowing existing LiDAR-based methods to be applied.
* **FCOS3D:** An anchor-free, fully convolutional single-stage network designed for monocular 3D object detection, directly predicting 3D bounding boxes from image features.

### 3. Multi-Modal Fusion Methods
These methods combine the strengths of different sensors, typically LiDAR and cameras, to achieve more robust and accurate detection.
* **Multi-view 3D (MV3D):** A two-stage fusion pipeline that generates object proposals from both LiDAR point clouds and camera images, then fuses features for accurate 3D box estimation.
* **Frustum PointNet:** A method that leverages mature 2D object detectors to generate 2D regions of interest (RoIs) in images. These RoIs are then used to extrude 3D frustums in the point cloud, significantly reducing the search space for 3D detection.
* **PointPainting:** A sequential fusion technique where semantic segmentation results from camera images are used to "paint" or augment LiDAR points with class-specific semantic information before feeding them into a 3D detector.

### 4. Hybrid and Graph-Based Methods
This category includes innovative approaches that combine different feature representations or utilize graph structures for detection.
* **Point-GNN:** A method that formulates 3D object detection as a task on graph neural networks, where a graph is constructed from the point cloud, and GNNs are used to predict bounding boxes.
* **PV-RCNN (Point-Voxel RCNN):** A high-performance detector that effectively combines the advantages of both voxel-based (for efficient feature encoding) and point-based (for flexible receptive fields) operations.

## 📊 Data Sources

The papers included in this visualization were systematically selected and analyzed from:

* **Major Computer Vision Conferences:** Proceedings from CVPR (Conference on Computer Vision and Pattern Recognition), ICCV (International Conference on Computer Vision), and ECCV (European Conference on Computer Vision).
* **Highly Cited arXiv Preprints:** Influential and foundational works that have significantly impacted the field, often appearing on arXiv before or alongside conference publication.
* **Citation Networks:** Tools like [ConnectedPapers.com](https://www.connectedpapers.com/) were used to identify related and influential works.

All selected papers were evaluated in the context of standard autonomous driving datasets such as **KITTI** and **nuScenes** to ensure relevance and allow for consistent benchmarking understanding.
