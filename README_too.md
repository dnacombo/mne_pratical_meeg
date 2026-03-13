# Dataset Introduction: Wakeman & Henson (2015)

**Title**: A multi-subject, multi-modal human neuroimaging dataset

**Authors**: Daniel G. Wakeman & Richard N. A. Henson

**Dataset Description**: This open-access dataset (often referred to by its OpenNeuro ID: ds000117) provides simultaneous recordings of **MEG, EEG, and fMRI** from 19 healthy participants. It was specifically designed as a "gold standard" benchmark for researchers developing methods for multimodal integration—the process of combining the high temporal resolution of electrophysiology (M/EEG) with the high spatial resolution of hemodynamics (fMRI).

**The Task**: Participants performed a **visual face-processing task**. They were shown three types of images: **Famous Faces, Unfamiliar Faces, and Scrambled Faces** (images where the phase information of a face was scrambled to create a meaningless texture with similar low-level visual properties).
##Detailed Task Introduction:

The dataset is particularly prized in the M/EEG community because of its high-quality **simultaneous EEG-MEG recordings** and its utility in studying the **N170/M170 component**—a specific brain response that occurs approximately 170ms after seeing a face.
###Experimental Protocol

- **Trial Structure**: Each stimulus was presented for approximately 800–1000 ms.
    
- **Participant Action**: To ensure they remained attentive to the visual details of the stimuli rather than just "categorizing" them, participants were asked to judge the left-right symmetry of each image by pressing one of two keys.
    
- **Trial Number**: The data includes 6 runs per subject, totaling nearly 300 trials per condition (Famous, Unfamiliar, Scrambled), providing a robust signal-to-noise ratio for Event-Related Potential (ERP) and Field (ERF) analysis.

###EEG/MEG Data Acquisition

- **MEG System**: Recorded using an Elekta Neuromag Vectorview 306-channel system. This includes 102 magnetometers (sensing magnetic field strength) and 204 planar gradiometers (sensing the spatial gradient of the magnetic field), which are more sensitive to local cortical activity.
    
 - **EEG System**: Recorded simultaneously using a 70-channel Easycap system (using a nose reference).
    
- **High Temporal Resolution**: Data were originally sampled at 1,100 Hz, allowing researchers to study not just the slow evoked components but also high-frequency oscillations (Gamma bands) and fine-grained connectivity between brain regions.

###Key Scientific Value

The primary goal of using this dataset is often Source Localization. By having the exact same task performed in fMRI (which shows where activity happens) and M/EEG (which shows when it happens), researchers can test algorithms that attempt to "map" the M/EEG signals back onto the cortical surface with the help of fMRI constraints.
