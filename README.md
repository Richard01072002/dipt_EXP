# Basics_image_manipulation 
### Name- RICHARDSON A
### reg no. - 212222233005
### dep - AI & DS 
## AIM
#### To manipulate the image in different patterns
## procedure 
#### Step 1: Install OpenCV
#### Step 2: Import Libraries: Import cv2 for image processing and matplotlib.pyplot for image display.
#### Step 3:Read Image: Use cv2.imread() to read the image file 'rocket.jpeg' in grayscale mode, storing it in the image variable.
#### Step 4: Get Dimensions: Retrieve the image dimensions (height and width) by accessing image.shape, and print these values.
#### Step 5: Display Image: Use matplotlib.pyplot to display the image in grayscale without axes.

#### Step 6: Save Image: Save the grayscale image as a PNG file named 'Apollo-11-launch.png' using cv2.imwrite().

## program
```
#EXP1
import cv2
import matplotlib.pyplot as plt 
# Read the image ('Apollo-11-launch.jpg') using OpenCV imread() as a grayscale image.
image = cv2.imread('rocket.jpeg', cv2.IMREAD_GRAYSCALE)
# Print the image width and height.
height, width = image.shape
print("Width:", width)
print("Height:", height)
# Displaying the image using matplotlib imshow().
plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.show()
# Save the image as a PNG file using OpenCV imwrite().
cv2.imwrite('Apollo-11-launch.png', image)
```
## OUTPUT 1
<img width="822" alt="Screenshot 2024-10-29 at 11 58 14 AM" src="https://github.com/user-attachments/assets/433fd080-c9d8-46a6-9037-cc7bc77aa910">


```
#EXP2
# Read the saved image above ('Emerald_Lakes_New_Zealand.jpg') as a color image.
image = cv2.imread('newlake.jpeg', cv2.IMREAD_COLOR)
# Print the image shape.
print("Image shape (color):", image.shape)
# Convert the image to grayscale using cv2.cvtColor().
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Print the grayscale image shape.
print("Image shape (grayscale):", gray_image.shape)
# Displaying the grayscale image using matplotlib imshow().
plt.figure(figsize=[10, 10])
plt.imshow(gray_image, cmap='gray')
plt.axis('off')
plt.show()
```
## OUTPUT 2
<img width="809" alt="Screenshot 2024-10-29 at 11 59 49 AM" src="https://github.com/user-attachments/assets/30e2029a-9f0d-450d-b17f-af98a04b3076">


```
#exp3
# Read the image ('New_Zealand_Boat.jpg') as a color image.
img = cv2.imread('lake.jpeg', cv2.IMREAD_COLOR)
# Display the original image.
plt.figure(figsize=[3, 3])
# Convert BGR to RGB for displaying with matplotlib
plt.imshow(img[:, :, ::-1])  
plt.axis('on')
plt.show()
# Crop the image to extract the region around the sailboat.
cropped_img = img[200:300, 300:450]
# Resize the image up by a factor of 2x.
resized_img = cv2.resize(cropped_img, (0, 0), fx=2, fy=2)
# Flip the cropped/resized image horizontally.
flipped_img = cv2.flip(resized_img, 1)
# Displaying the final result.
plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1]) 
plt.axis('off')
plt.show()
```
### OUTPUT 3
#### Display the original image.
<img width="331" alt="Screenshot 2024-10-29 at 12 00 37 PM" src="https://github.com/user-attachments/assets/25132683-9e6a-419a-b7d7-a81649bd803f">
<img width="410" alt="Screenshot 2024-10-29 at 12 01 00 PM" src="https://github.com/user-attachments/assets/288ec886-10b7-42e9-be43-1ce33456ebad">


```
#exp4
image = cv2.imread("rocket.jpeg")
fig, ax = plt.subplots()
ax.imshow(image)
ax.set_xticks(range(0, image.shape[1], 100))
ax.set_yticks(range(0, image.shape[0], 100))
plt.show()
image = cv2.imread("rocket.jpeg")
x, y = 500, 50
width = 200
height = 600
cv2.rectangle(image, (x, y), (x + width, y + height), (0, 0, 255), 3)
fig, ax = plt.subplots()
ax.imshow(image)
ax.set_xticks(range(0, image.shape[1], 100))
ax.set_yticks(range(0, image.shape[0], 100))
plt.show()

```
### Output 4
<img width="570" alt="Screenshot 2024-10-29 at 12 02 25 PM" src="https://github.com/user-attachments/assets/e716b4b7-4c74-48f5-94a2-2271fe6ed4b9">
<img width="301" alt="Screenshot 2024-10-29 at 12 03 39 PM" src="https://github.com/user-attachments/assets/c2289124-a6c8-4613-8f8d-67fa563d5dd8">
<img width="565" alt="Screenshot 2024-10-29 at 12 03 53 PM" src="https://github.com/user-attachments/assets/6b5667da-12b1-4456-98dc-7a2f12c86d6a">



### Result 
#### Running this code will display the grayscale image, print its dimensions, and saved 
