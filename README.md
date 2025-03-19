# Auto-UIT
## Abstract

- UAV-assisted inspection is critical for modern power grid maintenance, enhancing efficiency and safety in remote areas. However, automatically designing UAV inspection trajectories is challenging due to the cluttered inspection environments, small inspection targets, and pervasive obstacles. We propose Auto-UT, a novel method for generating inspection trajectories in noisy, sparse, and complex 3D point cloud. Auto-UT has three core techniques: (1) A local structure–enhanced pylon segmentation, which accurately segments pylons, power lines, and surroundings in noisy point cloud for effective inspection target identification and trajectory planning. (2) A 3D fingerprint–based pylon type recognition that compensates for point cloud sparsity to complete missing inspection targets based on the pylon type. (3) An adaptive trajectory generation that samples positions in response to diverse pylon orientations and pervasive environmental obstacles, ensuring UAV operational safety. 
  Our experiments demonstrate that Auto-UT outperforms existing baseline methods in all three tasks. Furthermore, a four-month deployment in a power grid inspection system—covering a 270 square kilometers primary mountainous area—yielded an expert first-review acceptance rate of 91.86% for the generated trajectories, and reduced design time by an average of 88.19% compared to manual methods, significantly improving inspection efficiency.

  

> 

---

## Demo Video

[![Watch the video](https://img.youtube.com/vi/XXXXXX/0.jpg)](https://anonymous.4open.science/r/Auto-UIT-2D87/video/demo.mp4)



### **About the Video**

In this video, we showcase **real-world collected point cloud data** and introduce our complete processing pipeline, including:

- **PySeg**: Pylon Segmentation module
- **PyRec**: Type Recognition module
- **TrajGen**: Trajectory generation module

The video provides a clear demonstration of the **workflow and corresponding results**.  

Additionally, we present the **Auto-UIT field deployment** and real-world **UAV inspection video**.  

---

##  Dataset

- We provide a labeled dataset for public use. The dataset is stored in the `data` folder, with each **point cloud file** saved in `.txt` format.  

  ### **🔹 Dataset Structure**

  - 📁 `data/` - Contains labeled point cloud data

  ### **🔹 Data Format**

  Each **point cloud file** is stored as a `.txt` file with the following columns:

  | Column  | Description                                                  |
  | ------- | ------------------------------------------------------------ |
  | 1st-3rd | `X, Y, Z` coordinates                                        |
  | 4th-6th | `R, G, B` color values                                       |
  | 7th     | **Semantic label** (0: surroundings, 1: Pylon, 2: Power Line) |

  > **🔹 Note:**  
  >
  > **All geographic information has been masked. All coordinate values are relative and do not represent any real-world locations.**  

---

### 


