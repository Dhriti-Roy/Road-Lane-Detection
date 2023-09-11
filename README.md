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

## Working
let’s take the single image frame below :
<img width="407" alt="image" src="https://github.com/Dhriti-Roy/Road-Lane-Detection/assets/74097309/f969043a-6609-4e30-8860-d73d245ee969">
In the above image, the lane markers are obvious to any human observer. We
perform processing of this image intuitively, and after being trained to drive a
human can detect the lane in which the vehicle appears to be moving. Humans also
effortlessly identify many other objects in the scene, such as the other vehicles, the
embankment near the right shoulder, some road signs alongside the road, and even
the mountains visible on the horizon. While many of these objects are complex in
visual structure, it could be said that the lane markers are actually some of the
simplest structures in the image!
Pre-existing knowledge of driving gives us certain assumptions about the properties
and structure of a lane, further simplifying the problem. One obvious assumption is
that the lane is oriented to be parallel with the direction of movement. This being the
case, the lines denoting the lane will tend to extend from the foreground of an image
into the background along paths that are angled slightly inwards.

### CROPPING TO A REGION OF INTEREST
#### LOADING AN IMAGE INTO MEMORY
#### Defining the Region of Interest
#### DETECTING EDGES IN THE CROPPED IMAGE
