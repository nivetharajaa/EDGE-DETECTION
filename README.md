# EX-06 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
Developed By:NIVETHA A

Register No: 212222230101
```
# Import the packages
import cv2

# Load the image, Convert to grayscale and remove noise
i=cv2.imread('land.jpeg',-1)
gray=cv2.cvtColor(i,cv2.COLOR_BGR2GRAY)
img = cv2.GaussianBlur(gray,(3,3),0)


# SOBEL EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
sobel_x=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
cv2.imshow('sobel_x',sobel_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_y=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
cv2.imshow('sobel_y',sobel_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
sobel_xy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
cv2.imshow('sobel_xy',sobel_xy)
cv2.waitKey(0)
cv2.destroyAllWindows()


# LAPLACIAN EDGE DETECTOR AND TO SHOW THE DETECTED IMAGE
rgb_image = cv2.cvtColor(i,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(rgb_image,cv2.CV_64F)
cv2.imshow('laplacian_operator',laplacian_operator)
cv2.waitKey(0)
cv2.destroyAllWindows()


# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(img, 120, 150)
cv2.imshow('canny',canny_edges)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### ORIGINAL IMAGE
![321913472-cd89118b-95d6-49b0-aa80-e01b6bd1e1f4](https://github.com/user-attachments/assets/ce6e3348-1f4b-4de0-a09c-16137da78a6e)

### SOBEL EDGE DETECTOR
![322020389-6cef316b-b83a-4843-b7c7-eb2cd15850d1-1](https://github.com/user-attachments/assets/7d8fb2ba-49a6-4876-b6a9-682ba31302c6)

![322020446-c1951fb9-e949-47a3-b3d1-935e7dc5e285-1](https://github.com/user-attachments/assets/a2834ab2-c4cb-40ea-b8e0-d5b5f0775908)

![322020492-e2e94e52-8827-44e0-826f-756d5bbf51f9](https://github.com/user-attachments/assets/36dd6469-bc0a-4f27-9925-c91db75dc5eb)

### LAPLACIAN EDGE DETECTOR
![322020631-82321c3a-bddf-4407-b306-7016395ee3e7](https://github.com/user-attachments/assets/e37ffbf5-bccc-4da4-bc4f-16d52f28eabf)

### CANNY EDGE DETECTOR
![322020687-d32ba108-76f7-481e-8fd5-344cd7ef6e4f](https://github.com/user-attachments/assets/1d320a81-1f07-4d30-b75b-30e6edcc9513)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
