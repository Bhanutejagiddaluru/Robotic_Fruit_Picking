# Robotic Fruit Picker Using Image Processing and Deep Neural Networks

Welcome to the **Robotic Fruit Picker** repository! This project develops an automatic fruit plucking drone to overcome labor shortages in agriculture. The system integrates **deep learning**, **image processing**, and **drone technology** to autonomously detect, classify, and harvest ripe fruits with minimal human intervention.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Architecture](#architecture)
4. [Goals](#goals)
5. [Fruit Detection System](#fruit-detection-system)
6. [Drone Control System](#drone-control-system)
7. [Gripper Mechanism](#gripper-mechanism)
8. [Notification System](#notification-system)
9. [Results](#results)
10. [Future Work](#future-work)
11. [Acknowledgements](#acknowledgements)

---

## Introduction

Agriculture is vital to global economies, but it faces challenges like **labor shortages** and **high labor costs**. These issues lead to fruit wastage as crops remain unharvested. This project aims to solve these problems by creating an **autonomous fruit-picking drone**. The system uses **deep neural networks** (CNN) to classify fruit as ripe, unripe, or rotten, and a **drone with a gripper** to pick the fruit.

---

## Project Overview

![Block Diagram](Goal2_Deep_learning_model_into_hardware.jpg)

The system consists of several key components:
- **Fruit Detection Unit**: Uses CNN to classify fruit based on images captured by a webcam or Pi-cam mounted on the drone.
- **Drone Unit**: A quadcopter equipped with a gripper for harvesting fruits from high tree branches.
- **Notification Unit**: Notifies the user about the ripeness of the fruit via **Pushbullet**.
- **Gripper Unit**: A robotic gripper mechanism that cuts the ripe fruit.

The system reduces the dependency on manual labor, speeds up harvesting, and prevents fruit wastage.

---

## Architecture

![Drone System Block Diagram](Goal5_drone_System.jpg)

- **Fruit Detection**: Captures images of the fruit using a **webcam** or **Pi-cam**, processes these images using **MATLAB** and a trained **AlexNet** model to identify the fruit's condition.
- **Drone Control**: A **Quadcopter** (Drone) is used to fly to the fruit and pick it. It is controlled using a **Fly Sky Transmitter-Receiver** system.
- **Gripper Mechanism**: The gripper is controlled to cut the ripened fruit using a **Fly Sky** controller.

---

## Goals

- **Goal 1**: Identify the fruit and determine if it is ripe.
- **Goal 2**: Transmit video data wirelessly for real-time monitoring.
- **Goal 3**: Send notifications for ripened fruit.
- **Goal 4**: Cut and harvest the ripened fruit.
- **Goal 5**: Enable drone flight for fruit harvesting.

---

## Fruit Detection System

The **fruit detection system** classifies fruit into categories: ripe, not ripe, or rotten. It uses a **Convolutional Neural Network (CNN)**, trained on a dataset of 7500 fruit images, to determine the ripeness of the fruit. This system is implemented on a **Raspberry Pi 4**, which captures the image using a **webcam**.

The dataset for training and testing comes from **Kaggle**, and the system uses **AlexNet** for fruit classification.

---

## Drone Control System

The **drone system** is a **quad copter** capable of flying to specific heights to access fruit on trees. The drone is equipped with:
- **A2212 DC Brushless Motors** for propulsion.
- **450mm Quad Frame** and **propellers** for stable flight.
- **SimonK 30A ESC** for motor control.
- **Tower Pro MG90s Servo** for controlling the gripper.

---

## Gripper Mechanism

Once a ripened fruit is detected, the **gripper unit** is activated. The **gripper**, controlled via a **Fly Sky transmitter**, cuts the ripened fruit from the tree. The gripper is equipped with **metal blades** and is controlled by a **digital servo motor**.

---

## Notification System

To notify the user when the fruit is ripe, the **MATLAB Pushbullet** feature is used. Notifications are only sent when the ripeness score exceeds **90%**. If the fruit is ripe, the user receives a message: "Ripen - cut the fruit." If not, the message reads: "Not Ripen - Do not cut the fruit."

![Goal 3 Notification](Goal3_notification_to_mobile.jpg)

---

## 📊 Results

![Confusion Matrix](Confusion_matrix.jpg)

The **AlexNet** model was trained with **7500 images**, achieving high accuracy. The **Confusion Matrix** shows that the system performs well, accurately distinguishing between ripe, unripe, and rotten fruits.

---

## Future Work

- **Improved Fruit Classification**: Incorporate more data to further enhance fruit classification.
- **Autonomous Harvesting**: Make the system fully autonomous, with minimal human intervention.
- **Adaptation for Different Fruit Types**: Extend the system to work with a broader range of fruits like mangoes.

---

## Acknowledgements

Special thanks to:
- **MATLAB** for providing the environment for deep learning training.
- **Kaggle** for the dataset.
- The authors of related works for their inspiration and contributions to the field of robotic fruit harvesting.

---

👋 **Thank you for exploring this repository!**
