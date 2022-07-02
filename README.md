# Cyber_security_and_Anonymization_of_CT_and_MRI_data
A collection of information and code pertaining to our cybersecurity and anonymization project for CT and MRI data at GW. 

Multiple previous studies have shown that patients can be identified from automated facial recognition software (or human viewers) based on 3-D reconstructions of computed tomography (CT) or magnetic resonance imaging (MRI) data. This presents a security concern for public data sets published online. 

Most datasets are deidentified by removing data from the Digital Imaging and Communications in Medicine (DICOM) headers without altering facial features. This makes evaluation of anonymization techniques and methods to identify weaknesses in public datasets (Such as if faces are still recognizable after brain or head and neck data is published online) to be paramount. 

We previously demonstrated that facial features (and consequently, faces) could be recognized by both a human observer and automated facial recognition software from beneath a thermoplastic simulation-CT (Sim-CT) mask used in radiation oncology. This demonstrated the ability to recognize faces not only from MRI, but also CT data in addition to the ability to recognize faces under a mask. 

See more here: https://www.sciencedirect.com/science/article/abs/pii/S1879850021002356

Our current research is focused on anonymization methods and tools to help other practitioners address this problem. 

Included code files:

**DICOM_Conversion**
Simple code to convert the surrounding voxels on a CT scan to mirror an MRIs so that the CT can be visualized or processed in software designed for T1W or T2W MRI.

**Generate_3D_Representation_of_Face** 
Stacks a series of DICOM files and then generates a 3D representation of the outline of person (and consequently - the face). 

**3D_Reconstruction_and_Facial_Identifier**
 Stacks a series of DICOM files,  generates a 3D representation of the outline of person (and consequently - the face), and runs a quick face recognition algorithm to see if the face is identifiable on the 3D reconstructed image. 

**Image_Matching_Methodology** 
Identifies total number of matched points between two images using FLANN and Brute Force Matcher. 

**Facial_Matching_Methodology**
Simple code to identify if two faces identified in two images match. 

**To cite this project or use any of the code please refer to the following publication:**


Provenzano, D., Loew, M. H., Goyal, S., & Rao, Y. J. (2022). Unmasking a Privacy Concern: Potential Identification of Patients in an Immobilization Mask from 3-Dimensional Reconstructions of Simulation Computed Tomography. In Practical Radiation Oncology (Vol. 12, Issue 2, pp. 120–124). Elsevier BV. https://doi.org/10.1016/j.prro.2021.09.006 
