# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
### Step2:
Read the image and convert the bgr image to gray scale image.
### Step3:
Use any filters for smoothing the image to reduse the noise.
### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
### Step5:
Display the filtered image using plot and imshow.

## Program:
### Import the packages and load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bike (1).jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```

### SOBEL EDGE DETECTOR
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.imshow(sobelx)
plt.title("SOBEL_X")
plt.xticks([])
plt.yticks([])
plt.show()
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.imshow(sobely)
plt.title("SOBEL_Y")
plt.xticks([])
plt.yticks([])
plt.show()
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.imshow(sobelxy)
plt.title("SOBEL_XY")
plt.xticks([])
plt.yticks([])
plt.show()
```

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.imshow(laplacian)
plt.title('LAPLACIAN')
plt.axis("off")
plt.show()
```

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(new_image, 120, 150)
plt.figure(figsize = (8,8))
plt.imshow(canny_edges)
plt.title('CANNY_EDGES')
plt.axis("off")
plt.show()
```

## Output:

### ORIGINAL
![pic1](https://user-images.githubusercontent.com/93427253/232083518-6868bdbf-318b-4889-b250-083e083af793.png)


### SOBEL EDGE DETECTOR
![pic2](https://user-images.githubusercontent.com/93427253/232083609-64297210-6243-4d63-970b-f022c942254e.png)
![pic3](https://user-images.githubusercontent.com/93427253/232083894-0b084f68-d2c0-4b62-8de1-7dfa8a7cea47.png)
![pic4](https://user-images.githubusercontent.com/93427253/232084095-dc7f90bd-9db7-49c4-b38f-230affaec575.png)


### LAPLACIAN EDGE DETECTOR
![pic5](https://user-images.githubusercontent.com/93427253/232084350-3f941bf8-932d-4e74-a31c-a1f3e63ec304.png)


### CANNY EDGE DETECTOR
![pic6](https://user-images.githubusercontent.com/93427253/232084424-30f05dd4-0ae5-4859-bbf3-9b40e44d69c6.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
