# COLOR_CONVERSIONS_OF-IMAGE
## AIM:
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:NARENDRAN B
### Register Number: 212222240069



### i) Read and display the image

```
       import cv2
    image=cv2.imread('flower.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('NAREN',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

 ## OUTPUT:

![WhatsApp Image 2024-05-07 at 11 10 29_97bb6e01](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/8280da28-3372-4dd6-ac24-4ae6caf6e1df)


### ii)Write the image
```
 image=cv2.imread('flower.jpg',0)
    cv2.imwrite('a.jpg',image)    

```
## OUTPUT:

![image](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/201374d8-0c1e-429f-93b6-0addb6df2322)


### iii)Shape of the Image
```
 import cv2
    image=cv2.imread('flower.jpg',1)
    print(image.shape)
```
## OUTPUT:
![image](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/03d86936-6c30-4aad-ad99-11c2c59c88d0)




### iv)Access rows and columns
```
        import random
    import cv2
    image=cv2.imread('flower.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('flower image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## OUTPUT:

![WhatsApp Image 2024-05-07 at 11 11 35_fd7e2a23](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/821b417f-936e-4810-a137-b16afa533c95)


### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## OUTPUT:

![WhatsApp Image 2024-05-07 at 11 12 46_877a95db](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/fabe6909-57a3-4205-b8ff-0ac452313c7b)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('flower.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## OUTPUT:
![WhatsApp Image 2024-05-07 at 11 13 19_1c22d2b8](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/746a350e-d54f-4cbd-9674-6d72cfa98ed6)



### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread("flower.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
![WhatsApp Image 2024-05-07 at 11 14 05_469a9961](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/a28efe05-c57b-48d8-a3ab-5cd44dcd3722)



### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('flower.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:

![image](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/ec44f202-0249-4b5a-a40a-391c75103d0a)

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('flower.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## OUTPUT:

![image](https://github.com/naren2704/COLOR_CONVERSIONS_OF-IMAGE/assets/118706984/d97cb7a8-65cf-40d0-9c97-65f50d55e0a4)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







