# Fundus-Imaging
Extracting blood vessels from retinal fundus images using classical morphological techniques.

Data is taken from the open source retinal database of the University of Erlangen-Nuremberg. 
Sample: 
![image](https://user-images.githubusercontent.com/53914842/140279666-58740fc9-1f41-4a73-be95-4e44608132be.png)


Firstly the green channel was isolated and extracted from the RGB image:
![image](https://user-images.githubusercontent.com/53914842/140279744-d3194c21-0605-4880-94db-4ab0bc6ca000.png)

Then to enhance, Contrast limited adaptive histogram equalization (CLAHE) was applied to the extracted green channel of the image. 
CLAHE applied image:
![image](https://user-images.githubusercontent.com/53914842/140279789-19342d13-afb1-4b10-afe0-6aee34437ffc.png)

Morphological closing and opening was performed on the CLAHE applied image 3 times with an elliptical kernel of sizes 5, 15 and 30. Then the final closed image was subtracted from the original image and was enhanced again with the help of CLAHE:

![image](https://user-images.githubusercontent.com/53914842/140279823-1b9426c9-4f6e-4f91-8b78-036e6b43d54b.png)


Subsequently contours were removed with the inbuilt funtions of OpenCV. 
![image](https://user-images.githubusercontent.com/53914842/140279873-4adf7981-f5ae-48eb-9424-bba1f8d3e6b1.png)

![image](https://user-images.githubusercontent.com/53914842/140279934-b236b1bf-26ae-4cba-8b55-335f3d91dc69.png)


The above mentioned process was applied on each of the 45 images through an automated process and the following performance metrics were performed:

Average root mean square error: 0.012812103579441706 

Average peak signal to noise ratio: 37.87098782126279

Average structural similarity index values: 0.8582882934168227
