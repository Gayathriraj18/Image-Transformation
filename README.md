# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
# Step1:
Import the required packages.

# Step2:
load the image file in the program.

# Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

# Step4:
Display the modified image output.

# Step5:
End the program.

## Program:
```
Developed By: Gayathri A
Register Number: 212221230028
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
img=cv2.imread('spi.jpg')
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(img)
plt.show()
rows,cols,dim=img.shape
```
i)Image Translation
```
m=np.float32([[1,0,100],[0,1,200],[0,0,1]])
t_img=cv2.warpPerspective(img,m,(cols,rows))
plt.axis('off')
plt.imshow(t_img)
plt.show()
```

ii) Image Scaling
```
n=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
s_img=cv2.warpPerspective(img,n,(cols*2,rows*2))
plt.axis('off')
plt.imshow(s_img)
plt.show()
```


iii)Image shearing
```
o_x=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
p_y=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sh_x=cv2.warpPerspective(img,o_x,(int(cols*1.5),int(rows*1.5)))
sh_y=cv2.warpPerspective(img,p_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sh_x)
plt.imshow(sh_y)
plt.show()
```


iv)Image Reflection
```
rows,cols,dim=img.shape
q_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
q_y=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
r_img=cv2.warpPerspective(img,q_x,(int(cols),int(rows)))
r_img1=cv2.warpPerspective(img,q_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(r_img)
plt.show()
plt.imshow(r_img1)
plt.show()
```



v)Image Rotation
```
angle=np.radians(40)
r=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
ro=cv2.warpPerspective(img,r,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(ro)
plt.show()
```



vi)Image Cropping
```
c_img = img[120:600,120:600]
plt.axis('off')
plt.imshow(c_img)
plt.show()
```
## Output:


![5 1](https://user-images.githubusercontent.com/94154854/232308711-9cd25b07-c4f1-4d52-b51c-a6d38e84dbce.png)


### i)Image Translation

![5 2](https://user-images.githubusercontent.com/94154854/232308723-fd62676a-a181-4bb7-a000-393290f01db3.png)


### ii) Image Scaling


![5 3](https://user-images.githubusercontent.com/94154854/232308731-b5bd8f3d-c7f8-4af4-8c6d-bea7d5211645.png)

### iii)Image shearing


![5 4](https://user-images.githubusercontent.com/94154854/232308746-552e08df-052a-422c-934c-e4c6c190367a.png)


### iv)Image Reflection

![5 5](https://user-images.githubusercontent.com/94154854/232308760-9870d3f4-1229-4022-a8e6-dbd195b621b2.png)

### v)Image Rotation

![5 6](https://user-images.githubusercontent.com/94154854/232308831-44c9ae16-eb58-46c0-8c48-35fb324940a8.png)

### vi)Image Cropping

![5 7](https://user-images.githubusercontent.com/94154854/232308835-afb70cd5-8a18-4bab-804d-ee81f24580d3.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
