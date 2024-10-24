---
layout: post
title: Meta Analysis
subtitle: Orbital Prosthesis Rehabilitation in Biomedical Engineering by Means of Computer Vision-Photogrammetry and 3D Prototyping
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/Final.png
share-img: /assets/img/path.jpg
tags: 
author: Sienna Correia
---

## Null and Alternative Hypotheses:
![The patient’s healthy and missing eye](/assets/img/InitialEye.png)
The null hypothesis is...
On the contrary, the alternative hypothesis is...


## Data Researchers
Mohammed R. Falih: 
Falih, currently working as a lecturer in the College of Engineering, University of Baghdad, conducted this research as part of his MSc studies. His work focused on rehabilitation approaches for maxillofacial deformities and the prototyping of orbital prostheses, aiming to provide alternative solutions to invasive methods in biomedical engineering applications. He was also primarily responsible for preparing the manuscript.
Fanar M. Abed:
Abed, a scientific researcher who received the B.Sc. degree in surveying engineering and the M.Sc. degree in photogrammetry from Baghdad University, Engineering College, Baghdad, supervised Falih's MSc research and played a key role in its development. She previously led research in photogrammetry and laser scanning at the College of Engineering, University of Baghdad, which forms the foundation of this study. Abed contributed significantly to the manuscript’s development, revision, and refinement.


## Referenced Datasets
The study references over 30 other relevant research reports including several written by the same author, Mohammed R. Falih. Critical information for this study was obtained from the previous research data. Several examples are outlined below and the studies are available to the public.

1. The Falih et al., 2021(Efficiency of +IDonBlender Photogrammetry Tool in Facial Prosthesis Rehabilitation) study performed an image quality test on the iphone camera sensor compared to the Nikon D7500, and Nikon D5200. The study proved that the iphone 11 pro max camera should be used for data acquisition. The study was also used to calculate the optimal data capture plan as part of their detailed image-network design. This included the selected Base-to-height (B/H) ratio of .65 and the use of about 8 levels of forming 4 main stations.

2. The Shamkhi and Abed, 2020 (Fusion of laser scans and digital images for effective cultural heritage conservation) study was referenced as part of the data acquisition section explaining why the more images captured from various locations is highly recommended to achieve accurate object coordinates. 

3. Matsuoka et al., 2019 pg 66-72 (Development of three-dimensional facial expression models using morphing methods for fabricating facial prostheses) was referenced in the introduction of the study describing drawbacks of traditional impression techniques that cause deformation of the facial topography surface due to the pressure or the weight of the impression material.


## Interest in the Study
The main goal of the study outlined in the paper is to explore how the photogrammetric technique, using computer vision-photogrammetry and 3D prototyping, can be a successful noninvasive and low-cost method for fabricating an orbital prosthesis for patients who have one healthy eye. The study will outline a detailed procedure which can then be used in the biomedical engineering field to create an automatic digital routine for the manufacturing of orbital prosthesis. The procedure will include the necessary photographic settings, the optimal capturing plan, and evaluation of the generated model.


## Recorded Data / Data Leftout
[A diagram to depict the method of data image capturing](/assets/img/PhotoCapturing.png)
The study uses the computer vision based Structure from Motion Multi View Stereo (SfM-MVS) photogrammetric technique to obtain an image based dataset and reconstruct a 3D model from 2D pictures. The patient's facial data was collected using an IPhone 11 Pro Max camera. 102 images at 4032 X 3024 resolution were captured from multiple camera exposure stations set at different angles and distances from the patient’s face to obtain overlapping images. 

[A data table with RMSE checkpoints](/assets/img/RMSE.png)
[A visual of the RMSE checkpoints from the dataset](/assets/img/VisualData.png)
This data is uploaded into the Metashape 3D reconstruction software that runs the Sfm algorithm to generate an accurate 3D model. The large number of overlapping images is important for accuracy, error detection and triangulation (mathematical method used to calculate the distances and relative 3D position (depth) of points in an image based on the different camera positions and the angles formed between the cameras and the object). The SfM algorithm uses the overlapping data to cross check feature matches, helping to reduce errors caused by poor lighting, human error, or other factors. As part of the Sfm-MVS algorithms the triangulation process also requires a large amount of overlapping data to create the high density point cloud of x,y and z coordinates representing the position in 3D space. This high density allows for a more detailed and accurate representation of the object’s surface capturing  intricate details such as textures and fine geometric features, which are necessary for creating accurate 3D models. 
The study is only interested in collecting data from the patients face therefore all other image data is ignored.


## Evidence to Support Conclusions
![The prosthesis on the eye](/assets/img/Final.png)
The author concluded that the prosthetics extraction-based computer vision photogrammetry “provides a high-accuracy digital impression that is subsequently used in fabricating prostheses virtually” (14, Conclusion) The recorded data depicts the accuracy by comparing  the image without prosthesis on page 09 Figure 04 to the end result with the generated prosthesis. (14, Figure 10) The accuracy can also be observed when examining the facial symmetry of the patient wearing the prosthesis.
The” high accuracy” of the digital impression was proven by both the RMSE checkpoint data and the 3Dreshaper evaluation of the match of the restored eye model with the original model.  Table 4 on page 11 showed the total RMSE error in the X and Y Coordinates to be highly acceptable at 0 .041 mm and 0.055 mm respectively and the color map on page 13, Figure 8 explained the error rate of the various optical area components.


## Funding
The paper did not outline funding however the research was part of the authors MSc studies in the College of Engineering at the Public University of Baghdad. Public research universities receive funds from the Government.  


## Perish or Public Effect on Study
The idea of publish or perish expresses the pressure faced by academics to publish their research. No, I don't think publish or perish had a major effect on the study. This study has over 30 referenced papers related to the study’s data collection and area of interest, as well as showing the timeline of the study (2013 to present).  Among the referenced papers, is an article that the principal investigator Falih, wrote alongside other researchers. (Falih,   M.R., Efficiency   of   +IDonBlender Photogrammetric   Tool   in   Facial   Prosthetics   Rehabilitation An Evaluation Study. Karbala International Journal of Modern Science, 2021) 
In 2021, Falih also wrote a study on The Value of Stereo-Photogrammetry and 3D Prototype Printing for Plastic and Reconstructive Surgery.
[https://www.researchgate.net/publication/368960995_The_Value_of_Stereo] Photogrammetry_and_3D_Prototype_Printing_for_Plastic_and_Reconstructive_Surgery

