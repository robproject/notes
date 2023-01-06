[until chapter 3](https://www.youtube.com/watch?v=WQeoO7MI0Bs)

### Get image
img = cv2.imread("dir/img.png")
for grayscale, pass '0'
cv2.imread("dir/img.png", 0)

### image attributes
img.shape = (int height, int width, int color-channels)

### image resize
cv2.resize(img,(int width, int height))
Scale:
cv2.resize(img, None, fx=2, fy=2)
### show image
cv2.imshow("title",img)
cv2.waitKey(0)

### crop image
img[int height start:int height stop, int width start:int width stop]

### warp perspective
paint gives pixel values

pts = np.float32([x1,y1],[x2,y2],[x3,y3],[x4,y4])
pts_defenition = np.float32([[0,0],[width,0],[0,height],[width,height]])
matrix = cv2.getPerspectiveTransform(pts,pts_defenition)
imgOutput = cv2.warpPerspective(img, matrix, (width,height))

### rotate
cv2.rotate(img, cv2.ROTATE_90_CLOCKWISE)
ROTATE_180

### threshold
cv2.threshold(image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)[1]
