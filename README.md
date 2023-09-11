# Road Lane Detection

The objective of this project is to implement and analyze a lane detection algorithm
that addresses the challenges mentioned above. The primary goals include:
Developing a lane detection pipeline that includes Canny edge detection, region of
interest selection, Hough line transform, averaging of detected lines, and
visualization of the results.
Enhancing the basic algorithm to handle curved lane markings through techniques
like polynomial fitting.Improving the algorithm’s robustness by implementing noise
reduction methods and considering adaptive thresholds for varying lighting
conditions. Visualizing the detected lanes accurately on the original video frames to
validate the algorithm’s effectiveness.

## Requirements:

Python 3.x
OpenCV (pip install opencv-python)

## Code Explanation:
display_lines(img, lines, line_length_factor=0.5):
This function draws detected lane lines on an image.
canny(img):
Performs edge detection on the input image.
region_of_interest(canny):
Masks the region of interest (ROI) on the edge-detected image.
houghLines(cropped_canny):
Applies Hough Transform to detect lines in the ROI.
addWeighted(frame, line_image):
Combines the original frame with the line image.
make_points(image, line):
Calculates the coordinates of the endpoints of a lane line.
average_slope_intercept(image, lines):
Calculates the averaged lane lines.

## Main loop:

Reads frames from a video file.
Applies edge detection.
Defines a region of interest.
Detects lines within the ROI.
Averages and draws the lines on the frame.
Displays the result.
Running the Script:
<img width="399" alt="image" src="https://github.com/Dhriti-Roy/Road-Lane-Detection/assets/74097309/23769208-1995-48f1-8d7f-e136bbf583ff">

Ensure you have a video file named "test5.mp4" in the same directory as the script or modify the cv2.VideoCapture argument to the path of your desired video file.
Exiting the Script:

Press q on the keyboard to exit the video window.

## Customization
You can adjust parameters like threshold, minLineLength, and maxLineGap in the houghLines function for fine-tuning the lane detection.

The region of interest can be modified in the region_of_interest function by changing the vertices of the triangle array.

## Example Output
The script will open a video window showing the original video with detected lane lines highlighted in red.
<img width="858" alt="image" src="https://github.com/Dhriti-Roy/Road-Lane-Detection/assets/74097309/f5d6e153-509f-4861-8cc7-b47408cabf92">


## Additional Notes
The accuracy of lane detection may vary depending on lighting conditions, road markings, and camera placement.

For optimal results, ensure the video feed contains clear and distinct lane markings.




