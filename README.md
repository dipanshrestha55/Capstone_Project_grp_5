
Group 5

Dipan Shrestha – S372122

Dylan Roy Tomlinson – S372936

Surendra Phuyal – S372088

Shishtata Bhandari – S370419

Supervisor:
Thuseethan Selvaraja



# Mango Disease Recognition using Deep Learning 

Mango production is one of the big industry of Norther Territory, and diseases affecting mangoes can have serious impact on the NT's economy. There have been many research and paper on plant pathology, but we decided to work on the current gap: a model using deep learning to classify images of mango leaves and find the diseased/healthy leaves. The goal is to support early detection of mango diseases to improve crop management and yield for NT.



## File Structure
Mango Disease Recognition using Deep Learning\
│
├── models\                       # Trained models (e.g., .keras files)   Note: latest model has the highest number
│   ├── 1.keras
│   ├── 2.keras
│   ├── 3.keras
│   └── 4.keras                   # Latest trained model
│
├── training\                     # Training-related files and source code
│   ├── mango_dataset\            # Dataset (Healthy / Diseased)
│   ├── mango_source_code\        # Python scripts, notebooks, etc.
│   ├── mangos_densenet201.keras  # Example trained model
│   ├── 4.keras                   # Trained model
│   └── .ipynb_checkpoints\       # Jupyter auto-saves
│
└── README.md / README.txt        # Project documentation



## Environment Requirements

The below is the requirement for the project. Ensure the following installed:

- Python 3.8 or higher
- TensorFlow 2.9+
- NumPy
- Matplotlib
- scikit-learn

Optional (depending on your workflow):
- Jupyter Notebook / JupyterLab

You can install the dependencies using:

```bash
pip install tensorflow numpy matplotlib scikit-learn jupyter
```


## Steps to Execute

1. Clone or download this repository.

2. Place your dataset in a folder named mango_dataset at the root directory. If you unzip the provided folder, the dataset will already be in place. The folder should follow the standard structure for image datasets.

3. Open Jupyter Notebook in the root directory and run the mango_source_code.ipynb file.

    The script will automatically:

4. Load and preprocess the dataset.

5. Build and compare multiple CNN models (e.g., MobileNetV2, DenseNet201) to select the best-performing one.

6. Train the selected model on your dataset.

7. Output accuracy and other evaluation metrics.


## Notes

- The code is designed to run in a Jupyter Notebook, with sections separated by comments (# ---- New Cell ----).

- You may need to adjust file paths depending on the location of your dataset.

- Enabling GPU support is recommended for faster training, though it is optional.


## About Dataset

Type of data: 240x320 mango leaf images
Data format: JPG

Number of images: 4000 images.
Distribution of instances: Each of the eight categories contains 500 images.

Diseases considered: The team concluded on these 7 diseases based on the information provided on the NT gov website: https://nt.gov.au/industry/agriculture/food-crops-plants-and-quarantine/fruit-crops/mango/pests-and-diseases and common Mango diseases found in other websites and research paper. Another deciding factor was the focus of the diseases as we focused on the leaves being the critical part of plants and visually detectable for the disease detection. Team went through all openly available datasets and compared them, checked on the consistency (having almost same number of pictures so it has no bias against disease dataset with less number of images).

Number of classes: Eight (including 7 diseases and 1 healthy category).

- Anthracnose
- Bacterial Canker
- Cutting Weevil
- Die Back
- Gall Midge
- Powdery Mildew
- Sooty Mould
- Healthy Leaves

Dataset Source: https://www.kaggle.com/datasets/aryashah2k/mango-leaf-disease-dataset/data

## Website
Once the model was finalised, it was integrated into a website where users/farmers can upload images and check the diseases along with some Recommended Suggestions for farmers. Plant Disease Recognition System is a powerful AI-powered web applicated designed as a draft for the possibility of future integration with a Flask backend. The process begins with model training and the automatic version saving directly into folder to maintain the reproductivity. The latest model is loaded into the Flask Application which runs locally. The website has an easy to understand UI design where users can either drag and drop images or upload from their files. Once the users upload the picture, the system analyses it in real time to show result of which class the disease belongs to along with treatment recommendations. The workflow from model preparation to user interaction is a pipeline for automated plant health diagnosis system that can be improved with more real-field images and model training.



## References
TensorFlow Documentation: https://www.tensorflow.org/tutorials/images/transfer_learning
