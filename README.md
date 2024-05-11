# Classification and Detection of Bearing Faults based on Vibration Signals using Transformers and Tsetlin Machines

This repository contains the code and documentation for a bachelor thesis focusing on the enhancement of bearing fault detection and classification systems using two machine learning models: the transformer, and the Tsetlin Machine (TM).

## These are the steps to train the models and generate results:

### Download Datasets
- [**NASA**](https://www.kaggle.com/datasets/vinayak123tyagi/bearing-dataset)
  - Download and extract into any folder.
- [**CWRU**](https://engineering.case.edu/bearingdatacenter/48k-drive-end-bearing-fault-data)
  - Download all files in the "Inner Race", "Ball", and "Centered @6:00" columns.
  - Put all files into one folder.

### Clone git repository
Either download the repo as ZIP folder,
or use ``git clone`` with the URL: 
``https://github.com/KnuteLute/Transformers_and_TsetlinMachines_for_Bearing_Faults.git``.

### Generate Spectrograms
- **NASA:**
  - Open ``Preprocessing->nasa_spectrograms.ipynb`` in a code editor that supports IPython notebooks.
  - Change value of ``NASA_root_folder`` to the folder the NASA dataset was extracted into.
  - Change value of ``NASA_spectrogram_output_folder_path`` to any empty folder to be used as the output folder for spectrogram data.
  - Run all code cells (last one is optional).
- **CWRU:**
  - Opern ``Preprocessing->cwru_spectrograms.ipynb`` in a code editor that supports IPython notebooks.
  - Change value of ``input_fodler_path`` to the folder the CWRU MATLAB files were downloaded into.
  - Change value of ``output_folder_path`` to any empty folder to be used as the output folder for spectrogram data.

### Train models

