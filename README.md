# Overview
At Colgate’s Foggy Bottom observatory, astronomers use finder images to locate astronomical objects and properly orient the telescope. This process is currently done by hand so it can sometimes take a long time to locate which area of the finder image the telescope points at. Automating this process using machine learning will speed up the observing process at Foggy Bottom. Through this project I hoped to find an artifical data generation pipeline which can be used to train a model to locate a telescope image in a larger telescope image. I believe I have a mostly succesful data generation pipeline. However, there are severe  limitations in representing the data as one image for a CNN In order for the machine to properly place a bounding box on the telescope location.

# Replication Instructions
- Begin by ensuring python 3 and conda are properly installed on your computer, then create a new envirnment for the project
- activate that environment and run the following command
```
conda install -c conda-forge astropy astroquery matplotlib pillow tensorflow pandas numpy seaborn -y
```
