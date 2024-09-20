---
title: "Overview"
permalink: /multi-agent-robust-pgo/
---
<div>
    <a href="https://github.com/AnshShah3009/gtsam_tutorials" target="_blank" style="display: inline-block; padding: 10px 15px; background-color: #24292e; color: #ffffff; border-radius: 5px; font-family: Arial, sans-serif; text-decoration: none;">
        <i class="fab fa-github" style="margin-right: 5px;"></i> View on GitHub
    </a>
</div>

## Introduction
The Multi-Agent Mapping with FinderNet and Graduated Non-Convexity project is a comprehensive endeavor aimed at revolutionizing the field of multi-robot mapping. This project stems from the challenges encountered in efficiently covering large areas with multiple robots, particularly dealing with issues related to data noise, outliers, and high communication bandwidth requirements.

## Challenges and Context
In the realm of multi-robot mapping, accurately determining the relative poses of robots is a persistent challenge. Traditional optimization techniques, such as Levenberg-Marquardt (LM) or Gauss Newton, while effective, often falter in the face of noisy data and outliers. Furthermore, these methods necessitate a precise initial guess and rely on sharing point clouds between robots, demanding high communication bandwidth and limiting the mapping range.

## Innovative Approach
To overcome these challenges, the project introduces an innovative approach by leveraging two key components: FinderNet and Graduated Non-Convexity (GNC).

### FinderNet
FinderNet, a deep learning-based loop detection system, operates efficiently in the latent space. This not only significantly reduces data transfer size to the central server but also excels in loop registration and detection. The efficiency gained from FinderNet is crucial in optimizing communication bandwidth, making it a standout feature of the project.

### Graduated Non-Convexity (GNC)
Integrated into the GTSAM framework, Graduated Non-Convexity (GNC) plays a pivotal role in enhancing outlier rejection during pose graph optimization. This integration contributes to the overall robustness and accuracy of the multi-agent mapping system.

## Key Components

### FinderNet
- Operates efficiently in the latent space, reducing data transfer size.
- Excels in loop registration and detection capabilities.
- Significantly optimizes communication bandwidth.

### Graduated Non-Convexity (GNC)
- Seamlessly integrated into the GTSAM framework.
- Enhances outlier rejection during pose graph optimization.
- Contributes to the overall robustness and accuracy of the mapping system.

## Evaluation and Validation
Thorough evaluations using diverse datasets are conducted to assess the performance of the proposed approach. The project showcases its ability to produce high-quality maps and achieve accurate localization, even in the presence of outliers. Various optimizers are employed to generate final maps, providing a comparative analysis of the project's effectiveness.

## Simulations with Husky Robots
To validate the practical applicability of the approach, simulations are conducted using the Husky robot in an indoor office environment. The showcased results demonstrate the method's precision in map creation while effectively handling outliers in loop closures. This real-world simulation enhances the credibility and applicability of the project.

## Conclusion
In conclusion, the Multi-Agent Mapping with FinderNet and Graduated Non-Convexity project presents a groundbreaking solution to the challenges posed by noisy data and communication bandwidth limitations in multi-robot mapping. Through the integration of FinderNet and GNC, the project not only addresses these challenges but also sets a new standard for map quality and localization accuracy in diverse scenarios. The comprehensive evaluation and real-world simulations validate the practical viability of the approach, positioning it as a noteworthy advancement in the field of multi-agent mapping.
