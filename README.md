# Medical-Imaging-Practical

## Overview
This repository contains a Jupyter Notebook for Medical Imaging. It demonstrates basic image processing techniques for medical images using Python and key libraries such as `pydicom`, `skimage`, and `matplotlib`. It includes functions to:

- Load and inspect DICOM metadata
- Map pixel values to meaningful units
- Apply windowing for tissue visualisation
- Enhance contrast and adjust intensity
- Identify and measure regions of interest
- Convert DICOM images for analysis
- Visualise and export processed images

## Requirements
Before running the notebook, ensure the following packages are installed:
- numpy==1.26.3
- pandas==2.2.0
- matplotlib==3.8.2
- pydicom==3.0.1
- scikit-image==0.22.0

  You can install missing dependencies using:
```sh
pip install -q numpy==1.26.3 pandas==2.2.0 matplotlib==3.8.2 pydicom==3.0.1 scikit-image==0.22.0
```

## Program Structure

<img width="3006" height="1411" alt="Program structure" src="https://github.com/user-attachments/assets/3d1e4150-dd95-4741-9abe-bcd41f9fea69" />


## Findings
This outlines the methods and findings from the analysis of CT scans, focusing on
techniques essential for enhancing medical images and assisting in the diagnosis of
COVID-19-related changes in lung tissues. Contrast enhancement was applied to the
scans, improving the clarity and visibility of lung structures. This adjustment is crucial for
detailed examination and accurate diagnosis. Statistical data was used to identify
variations in pixel distributions, and histograms aided in quantifying and visualising
tissue density. Additionally, the use of coronal reconstructions and maximum intensity
projections provided di[erent perspectives on the lung structures, o[ering a more
comprehensive view that is beneficial for clinical assessments. These analyses can help
to understand the extent and nature of lung damage and track lung changes associated
with COVID-19 if the data is compared over time.

## Images
<img width="4400" height="1337" alt="Task_2_3_Axial_slice_A_normal_windowed" src="https://github.com/user-attachments/assets/565fcaf2-639e-400c-8d4a-14488cec608b" />
Axial CT image for patient A, taken from the middle of the body, original [1], transformed into Hounsfield
Units [2] and enhanced and windowed with a focus on lung tissue [3].

<img width="3145" height="2637" alt="Task_4_Histograms_pixel_intensity_A_B" src="https://github.com/user-attachments/assets/79b97d07-0f27-4cbb-a18f-351c4701ebb2" />
Histograms for the pixel distribution for an example scan for patient A [1], all scans for patient A [2], all scans
for patient B [3], and all the scans of patients A and B [4].

<img width="3630" height="1022" alt="Task_6_Coronal_slices_windowed_A_B" src="https://github.com/user-attachments/assets/57bd9f55-ed46-4367-9218-d0242df3ed61" />
Coronal slices from the middle for patients A [1] and B [2], enhanced to better visualise the anatomical
details.

<img width="3839" height="1002" alt="Task_7_MIP_coronal_A_B_windowed" src="https://github.com/user-attachments/assets/78d8c355-bc11-4486-a194-d138dcd09db1" />
Windowed coronal MIP for patients A [1] and B [2] stacked from 40 slices.

<img width="3535" height="1569" alt="Task_8_MIP_axial_A_B" src="https://github.com/user-attachments/assets/fb8d5d7b-82af-4e61-979b-2c3c02ead57e" />
Axial MIP for patients A [1] and B [2] stacked from 50 slices.


## Challenges
However, for practical application in clinical settings with multiple patient datasets,
improvements in the code structure are necessary. The current method uses numerous
individual variables for each patient, which reduces the code's readability and scalability.
A consistent modular approach, where each process is encapsulated in functions, would
improve reproducibility and maintainability. Additionally, issues with lung segmentation
need addressing to prevent errors in calculating lung tissue in the scans, particularly in
the peripheral and central slices.



