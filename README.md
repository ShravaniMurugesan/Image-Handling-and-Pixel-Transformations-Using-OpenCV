# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
 ## Name:SHRAVANI M
 ## Register Number:212224230263

  ## Ex. No. 01
```
import cv2
import matplotlib.pyplot as plt
```
```python
# Read the image using OpenCV
img = cv2.imread('photo.jpeg', cv2.IMREAD_COLOR)
```
```python
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

```python
# Display the image using matplotlib imshow().
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
## OUTPUT :

<img width="356" height="417" alt="image" src="https://github.com/user-attachments/assets/6d96f7ad-9d5f-4ec6-a81e-ca14de388654" />


```python
# Load the image
image = cv2.imread('photo.jpeg') 
```
```python
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```

<img width="244" height="43" alt="image" src="https://github.com/user-attachments/assets/d25ddf8f-aba8-498f-9fab-6e8c3245e94c" />

```python
# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

## OUTPUT :



```python
# Load the image
image = cv2.imread('photo.jpeg')

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape

```
## OUTPUT :

<img width="397" height="421" alt="image" src="https://github.com/user-attachments/assets/65eb79ae-0858-49a3-afb5-0a75d43f4b9d" />


```
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
```

```python
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="387" height="413" alt="image" src="https://github.com/user-attachments/assets/31e2cc05-fe2d-4026-b93a-296e9d5d88b9" />


```
# Load the image
image = cv2.imread('photo.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
```

<img width="233" height="42" alt="image" src="https://github.com/user-attachments/assets/4e124fc0-a314-4e0d-8b77-814ce105e62f" />

```python
# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="353" height="417" alt="image" src="https://github.com/user-attachments/assets/7cb79e1a-459a-485f-978d-67bdcb36d545" />


```
# Load the image
image = cv2.imread('photo.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
```
# Add text to the image
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
```
```
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="392" height="412" alt="image" src="https://github.com/user-attachments/assets/f60fecab-9650-4402-92d0-1e3fade3d4b7" />


```python
# Load the image
image = cv2.imread('photo.jpeg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
```python
# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```
## OUTPUT : 

<img width="355" height="412" alt="image" src="https://github.com/user-attachments/assets/e0355880-ac05-4005-9726-a990f04fd90a" />

```python
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

# OUTPUT :

<img width="322" height="432" alt="image" src="https://github.com/user-attachments/assets/5e18435b-1f8c-41ba-9845-d6877d75898c" />


```python
# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
```
```python
# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

## OUTPUT :

<img width="377" height="425" alt="image" src="https://github.com/user-attachments/assets/7e6feebb-8c9d-415e-9cdd-4ba2a58f9032" />


```python
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
```
```
# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

## OUTPUT :

<img width="322" height="417" alt="image" src="https://github.com/user-attachments/assets/36a65163-08e1-41b5-b76a-da00ab1c0157" />


```python
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

## OUTPUT :

<img width="357" height="413" alt="image" src="https://github.com/user-attachments/assets/417f80df-5a2a-4fdb-8c74-2fc805f7ccb2" />


```python
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499

# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
```
# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

## OUTPUT :

<img width="397" height="422" alt="image" src="https://github.com/user-attachments/assets/1c9dd305-55b4-4117-b0d3-7d395fa3d6dd" />


```
# Load the image
image = cv2.imread('photo.jpeg')
image.shape
```
<img width="183" height="44" alt="image" src="https://github.com/user-attachments/assets/877e33d2-5758-43bb-b338-d7e2933874ec" />

```
# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)

# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
```

<img width="199" height="44" alt="image" src="https://github.com/user-attachments/assets/ae8f2ba6-05c1-44e6-83e4-b274aac15330" />

```
# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

## OUTPUT :

<img width="558" height="422" alt="image" src="https://github.com/user-attachments/assets/2bee8c2c-1f4f-4294-a4e5-729cdd1af873" />


```
# Load the image
image = cv2.imread('photo.jpeg')
image.shape
```
<img width="204" height="48" alt="image" src="https://github.com/user-attachments/assets/e9d9fcba-6eaa-428d-813b-581e412d6358" />

```
# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
```
```
# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
## OUTPUT :

<img width="432" height="415" alt="image" src="https://github.com/user-attachments/assets/b703f2d4-0e6a-408a-b91d-58c9fbc4a50a" />


```
# Load the image
image = cv2.imread('photo.jpeg')

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)

# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
```
```
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
## OUTPUT :

<img width="382" height="410" alt="image" src="https://github.com/user-attachments/assets/abd8ad99-4654-4649-9dcd-63c7031ebc94" />


```
# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)

# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
```
```
# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
## OUTPUT :

<img width="351" height="376" alt="image" src="https://github.com/user-attachments/assets/6a87caf3-d172-44ea-82bd-c5dbcd35038e" />


## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

