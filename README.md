# Milestone 1
In the notebook below I have created a pipeline for generating artificial data to be used in training for Telescope image finding on finder images. Thus far I have better learned how to use os, how to write to JSON files, and image processing using pillow.

The pipeline works as follows:
- using RA and Dec coordinates to retrieve 60'x 60' finder images SkyView 
- put any generated images in the *finder_images* folder
- create the telescope image by croping the finder image, fliping the image horizontally, increasing contrast, adding gaussian noise
- add each of these images to the *telescope_images* folder
- write the path of the finder image, telescope image, and area of the crop to a JSON file 
