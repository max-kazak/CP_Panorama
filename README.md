# Panoramas

## Synopsis

In this project, I'm writing code to align & stitch together a series of images into a panorama.


## Directions

- Images in the `images/source/sample` directory are provided for testing 

- Downsampling your images to 1-2 MB each will save processing time during development. (Larger images take longer to process, and may cause problems for the VM and autograder which are resource-limited.)

- To execute panorama pipeline execute `python main.py`. The script will look inside each subfolder under `images/source` and attempt to apply the panorama procedure to the contents, and save the output to a folder with the same name as the input in `images/output/`. (For example, `images/source/sample` will produce output in `images/output/sample`.)


### 1. Implement the functions in the `panorama.py` file.

  - `getImageCorners`: Return the x, y coordinates for the four corners of an input image
  - `findHomography`: Return the transformation between the keypoints of two images
  - `getBoundingCorners`: Find the extent of a canvas large enough to hold two images
  - `warpCanvas`: Warp an input image to align with the next adjacent image
  - `blendImagePair`: Fit two images onto a single canvas


### 2. Generate your own panorama

Choose a scene for your panorama and capture a sequence of at least three (3) partially overlapping frames spanning the scene. Your pictures should be clear (not be blurry) for feature matching to work well, and you should make sure you have substantial overlap between your images for best results. You will need to explore different feature matching and keypoint settings to improve your results, and to record your modifications and parameter settings in your report (see the report template).
