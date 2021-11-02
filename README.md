# Fundus-Imaging
Extracting blood vessels from retinal fundus images using classical morphological techniques. 
Data is taken from the open source retinal database of the University of Erlangen-Nuremberg. Firstly the green channel was extracted from the RGB image. Then to enhance, Contrast limited adaptive histogram equalization (CLAHE) was applied to the extracted green channel of the image. 
Morphological closing and opening was performed on the CLAHE applied image 3 times with an elliptical kernel of sizes 5, 15 and 30. Then the final closed image was subtracted from the original image and was enhanced again with the help of CLAHE.

Subsequently contours were removed with the inbuilt funtions of OpenCV. 
The above mentioned process was applied on each of the 45 images through an automated process and the following performance metrics were performed:

Average root mean square error: 0.012812103579441706 

Average peak signal to noise ratio: 37.87098782126279

Average structural similarity index values: 0.8582882934168227
