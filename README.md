## Laundry_Microplastic_Characterization
# Purpose
To run this script, you'll need Python installed on your system along with several dependencies:
* numpy
* pandas
* cv2 (OpenCV)
* matplotlib
* skimage
* scipy

You can install these dependencies using pip:
`pip install numpy pandas opencv-python matplotlib scikit-image scipy`
# Installation 
No specific installation steps are required for the script itself, just ensure all dependencies are installed.
# Usage 
To use the script, load your filter paper images or use one of the example images in the Zenodo file. For each filter paper image, the parameters of the circular crop must be adjusted to achieve the maximal filter paper area is shown. This is done by changing the `border`, `right_shift`, and `down_shift` parameters. The amount of Gaussian blurring in the background subtraction procedure can be adjusted by changing the `filter_width` variable. The Gaussian-offset threshold can be adjusted to change the number of standards of deviation from the background peak used to segment the microplastics by modifying the multiplier in the `thresh` variable. The minimal size of microplastics counted can be adjusted with the `large_contour_threshold` variable in the contour detection section. 
# Inputs 
Filter paper images should be input as .TIF files with a square aspect ratio. They should contain dark particles on a light, circular filter paper background. The sample image (Test_Image.TIF), any of the full filter paper images (https://zenodo.org/records/10806174), or you own image can be used for the analysis.
# Outputs  
The script outputs the number of fibrous particles above a size threshold within the image. It can also export an image of the filter paper with annotations for the counted particles and a .xlsx file containing the total number of particles, the number of large particles, and the area of each particle in pixels. 
