# Classification and Detection of Bearing Faults based on Vibration Signals using Transformers and Tsetlin Machines
#### Simon Makassiouk, Knut Selstad, Sigurd Søberg

This repository contains the code and documentation for a bachelor thesis focusing on the enhancement of bearing fault detection and classification systems using two machine learning models: the transformer, and the Tsetlin Machine (TM).

ChatGPT by OpenAI was used to assist in implementing code.

These are the steps to train the models and generate results:
## Download Datasets
- [**NASA**](https://www.kaggle.com/datasets/vinayak123tyagi/bearing-dataset)
  - Download and extract into any folder.
- [**CWRU**](https://engineering.case.edu/bearingdatacenter/48k-drive-end-bearing-fault-data)
  - Download all files in the "Inner Race", "Ball", and "Centered @6:00" columns.
  - Put all files into one folder.

## Clone Git Repository
Either download the repo as ZIP folder,
or use ``git clone`` with the URL: 
``https://github.com/KnuteLute/Transformers_and_TsetlinMachines_for_Bearing_Faults.git``.

## Generate Spectrograms
- **NASA:**
  - Open ``Preprocessing->nasa_spectrograms.ipynb`` in a code editor that supports IPython notebooks.
  - Change value of ``NASA_root_folder`` to the folder the NASA dataset was extracted into.
  - Change value of ``NASA_spectrogram_output_folder_path`` to any empty folder to be used as the output folder for spectrogram data.
  - Run all code cells (last one is optional).
- **CWRU:**
  - Opern ``Preprocessing->cwru_spectrograms.ipynb`` in a code editor that supports IPython notebooks.
  - Change value of ``input_fodler_path`` to the folder the CWRU MATLAB files were downloaded into.
  - Change value of ``output_folder_path`` to any empty folder to be used as the output folder for spectrogram data.

## Train Models
### Tsetlin Machine Models
There are 9 scripts for TM models:
- **CWRU:**
  - ``CWRU_CTM_thermometer.ipynb``: Convolutional Tsetlin Machine (CTM) using thermometer embedding.
  - ``CWRU_MTM_AGT.ipynb``: Multiclass Tsetlin Machine (MTM) using Adaptive Gaussian Thresholding (AGT).
  - ``CWRU_MTM_AGT_explainable.ipynb``: MTM using AGT with additional code to generate clause activation heatmap.
  - ``CWRU_MTM_binary.ipynb``: MTM using binary embedding.
  - ``CWRU_MTM_thermometer.ipynb``: MTM using thermometer embedding.
- **NASA:**
  - ``NASA_CTM_thermometer.ipynb``: Convolutional Tsetlin Machine (CTM) using thermometer embedding.
  - ``NASA_MTM_AGT.ipynb``: Multiclass Tsetlin Machine (MTM) using Adaptive Gaussian Thresholding (AGT).
  - ``NASA_MTM_binary.ipynb``: MTM using binary embedding.
  - ``NASA_MTM_thermometer.ipynb``: MTM using thermometer embedding.

All scripts for TM models are structured similarly. To run any of them, follow these steps:
- **CWRU:**
  - Open script from ``TsetlinMachine->CWRU`` in a code editor that supports IPython notebooks.
  - Change value of ``directory_path`` to the folder chosen as output folder for spectrograms during preprocessing (value that ``output_folder_path`` was set to in ``Preprocessing->cwru_spectrograms.ipynb``).
  - Optionally change the value of ``json_file`` to desired directory to save results to.
  - Run all code cells.
- **NASA:**
  - Open script from ``TsetlinMachine->NASA`` in a code editor that supports IPython notebooks.
  - Change value of ``NASA_spectrogram_root_folder`` to the folder chosen for spectrograms during preprocessing (value that ``NASA_spectrogram_output_folder_path`` was set to in ``Preprocessing->nasa_spectrograms.ipynb``).
  - Optionally change the value of ``json_file`` to desired directory to save results to.
  - Run all code cells.

### Transformer Models
There are two scripts for transformer models:
- ``CWRU_Transformer.ipynb``
- ``NASA_Transformer.ipynb``

To run either of them, follow these steps:
- Open script from ``Transformer`` in a code editor that supports IPython notebooks.
- Change value of ``NASA_spectrogram_root_folder`` to the folder chosen for spectrograms during preprocessing (value that ``NASA_spectrogram_output_folder_path`` was set to in ``Preprocessing->nasa_spectrograms.ipynb``).
- Run all code cells.
