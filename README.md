# SALSA: System for Automatic liver Lesion Segmentation And detection

This is the code repository of the liver tumor automatic detection and segmentation tool by Dr. Raquel Perez-Lopez and colleagues from the Radiomics group at the Vall d'Hebron Institute of Oncology (VHIO), Barcelona, Spain.

<p align="center">
    <img src=imgs/workflow.png width="700" height="561.97">
</p>


**🚧 WORK IN PROGRESS 🚧**


## Requirements
Download or clone this repository as follows, and navigate into the new folder /liver-SALSA:

`git clone https://github.com/radiomicsgroup/liver-SALSA`

You may create a new Python environment, we will use anaconda/miniconda:

`conda create --name myenv python=3.8`

`conda activate myenv`

Install python packages specified in the file requirements.txt from the liver-SALSA folder:

`pip install -r requirements.txt`


A Docker file is in development for a more swift implementation

## Content
- `SALSA_stepONE.py`: code that contains the functions to load and preprocess the data.
- `SALSA_stepTWO.py`: code for running our trained model on the preprocessed data and to save and postprocess the final mask.
- `run_SALSA.py`: code to run the pipeline.

If you want to access to the model's weights please contact us! (mbalaguer@vhio.net or adriamarcos@vhio.net)


## Usage
To run the pipeline, call `python run_SALSA.py`:

`python run_SALSA.py -i /path_to_input_image`

The input to the pipeline can be:
* The path to the image to be segmented in NIfTI format (.nii or .nii.gz). 
* A csv with all the desired paths of the images to be segmented.


The output segmentation file will also be in NIfTI format. The new file will be saved in the same directory at the same level as the image, with the same filename adding '_SALSA' at the end.

See all options in the `python run.py --help`



## License
Please, see `license.txt`


## Citation
The paper is currently under review, a preprint version of the article is available at http://dx.doi.org/10.2139/ssrn.4890104


If you have questions please contact Dr. Raquel Perez-Lopez (rperez@vhio.net), Maria Balaguer (mbalaguer@vhio.net) or Adrià Marcos (adriamarcos@vhio.net).

To know more about our group, visit us at https://radiomicsgroup.github.io