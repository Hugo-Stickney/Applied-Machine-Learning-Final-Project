# Overview
At Colgate’s Foggy Bottom observatory, astronomers use finder images to locate astronomical objects and properly orient the telescope. This process is currently done by hand so it can sometimes take a long time to locate which area of the finder image the telescope points at. Automating this process using machine learning will speed up the observing process at Foggy Bottom. Through this project I hoped to find an artifical data generation pipeline which can be used to train a model to locate a telescope image in a larger telescope image. I believe I have a mostly succesful data generation pipeline. However, there are severe  limitations in representing the data as one image for a CNN In order for the machine to properly place a bounding box on the telescope location.

# Replication Instructions
- Begin by ensuring python 3, jupyter notebook, and conda are properly installed on your computer, then create a new envirnment for the project
- activate that environment and run the following command
```
conda install -c conda-forge astropy astroquery matplotlib pillow tensorflow pandas numpy seaborn -y
```
- create a new folder on your computer and download both attached .ipynb files into the folder
- open up `data_generation.ipynb` in jupyter notebook and run each cell in order
- after the Kernel finishes open `data_processing.ipynb` in jupyter notebook and run each cell in order picking only one model at a time
- note that you should either run Model 1, Model 2, or Model 3. **running all 3 of these cells will not achieve the desired results**
- this pipline allows for easy addition of other models and easy expansion of the dataset

# Future Directions
There are many ways to improve the work presented in this project. On my computer I had very limited space for a generated dataset so it might be interesting to expand the dataset to from 1,000 images to test if models fail on a larger dataset. The code could also very easily chnage to move from single-image representation to multi-input representation and changing models accordingly. I suspect the task fails due to a loss of fine detail in the images. This presents an issue in images of stars where very fine detail is important so if downsampling could be reduced to better handle small astronomical features models might perform better. I also thing the data generation for the telecope images could be more physically accurate to behaviors of actual telescope imaging. This could be done with physically based noise replacing the gaussian noise and more research being done into a physical basis for darkening the image.

# Contributions
- Research and preperation: 2 hours
- Data Generation Pipeline: 4 hours
- Initial Model Fitting: 4 hours
- Trying Other Models: 3 hours

Total: 13 hours

