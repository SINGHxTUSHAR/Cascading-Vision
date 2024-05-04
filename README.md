[![GitHub license](https://img.shields.io/github/license/SINGHxTUSHAR/Cascading-Vision.svg)](https://github.com/SINGHxTUSHAR/Cascading-Vision/blob/master/LICENSE)
[![GitHub contributors](https://img.shields.io/github/contributors/SINGHxTUSHAR/Cascading-Vision.svg)](https://GitHub.com/SINGHxTUSHAR/Cascading-Vision/graphs/contributors/)
[![GitHub issues](https://img.shields.io/github/issues/SINGHxTUSHAR/Cascading-Vision.svg)](https://GitHub.com/SINGHxTUSHAR/Cascading-Vision/issues/)
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/SINGHxTUSHAR/Cascading-Vision.svg)](https://GitHub.com/SINGHxTUSHAR/Cascading-Vision/pulls/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)


[![GitHub watchers](https://img.shields.io/github/watchers/SINGHxTUSHAR/Cascading-Vision.svg?style=social&label=Watch&maxAge=2592000)](https://GitHub.com/SINGHxTUSHAR/Cascading-Vision/watchers/)
[![GitHub forks](https://img.shields.io/github/forks/SINGHxTUSHAR/Cascading-Vision.svg?style=social&label=Fork&maxAge=2592000)](https://GitHub.com/SINGHxTUSHAR/Cascading-Vision/network/)
[![GitHub stars](https://img.shields.io/github/stars/SINGHxTUSHAR/Cascading-Vision.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/SINGHxTUSHAR/Cascading-Vision/stargazers/)

[![Open in Visual Studio Code](https://img.shields.io/static/v1?logo=visualstudiocode&label=&message=Open%20in%20Visual%20Studio%20Code&labelColor=2c2c32&color=007acc&logoColor=007acc)](https://open.vscode.dev/SINGHxTUSHAR/Cascading-Vision)

# Cascading-Vision 🚗:
![img_usedTO](https://github.com/SINGHxTUSHAR/Cascading-Vision/assets/113624520/3b0993d1-a2c6-4380-b4ee-05964bd02630)


Car number plate detection with Haar Cascade classifiers is a technique for identifying car plates in images and videos. It works by using a pre-trained classifier that has learned to recognize specific features common to number plates. This classifier, typically stored in an ".xml" file, acts like a template to find matching patterns within an image.

The process starts by converting the image to grayscale, since color information isn't essential for this task. Then, the classifier scans the grayscale image, searching for features that align with its understanding of a number plate. If a matching region is found, a rectangle is drawn around the detected area, indicating the likely location of the car's number plate.

Haar Cascade classifiers are popular for this application because they're relatively fast and efficient, making them suitable for real-time processing. They're also easier to implement compared to more advanced techniques. However, their accuracy can be limited by factors like variations in lighting, plate angles, or even different plate formats. Additionally, the classifier might sometimes mistake similar shapes for number plates, leading to false detections.

While Haar Cascades offer a good starting point for car number plate detection, especially for situations with limited resources, achieving higher accuracy and robustness might require exploring deeper learning techniques like YOLO.


## Work-Flow ⚔️:

### Preparation:

* `Install libraries:` Ensure you have OpenCV and NumPy installed. These libraries provide the image processing and computer vision functionalities needed.
* `Load the classifier:` Download a pre-trained Haar cascade classifier specifically designed for car number plates. These are typically ".xml" files and can be found online from various sources (ensure they are reputable).

### Image Processing:

* `Load the image:` Use OpenCV's cv2.imread function to read the image containing the car you want to detect the plate from.
* `Convert to grayscale:` Color information isn't crucial for number plate detection, so convert the image to grayscale using cv2.cvtColor. This reduces processing time and simplifies the analysis.

### Detection with Haar Cascade:

* `Instantiate the classifier:` Create a Haar cascade classifier object using cv2.CascadeClassifier and provide the path to the downloaded ".xml" file.
* `Detect plates:` Use the detectMultiScale function of the classifier object on the grayscale image. This function searches for regions in the image that match the classifier's idea of a number plate. It returns a list of rectangles representing the bounding boxes around the detected plates.

### Result Processing (Optional):

* `Iterate through detections:` Loop through the list of rectangles returned by detectMultiScale.
* `Draw bounding boxes (visualization):` Use OpenCV's drawing functions like cv2.rectangle to draw a rectangle around each detected plate on the original color image (optional for visualization purposes). You can also extract the coordinates of the bounding box for further processing.
* `Filter detections (advanced):` You can implement additional filtering steps to improve accuracy. This might involve checking the aspect ratio of the bounding boxes (since plates typically have a specific width-to-height ratio) or applying simple color thresholding to focus on areas with high contrast (like the text on the plate).

### Output:

* `Display the image:` Use cv2.imshow to display the original image with the drawn bounding boxes (if visualization was enabled).
* `Extract plate regions:` For further processing like character recognition, you can use the coordinates of the bounding boxes to crop out the detected plate regions from the original image.

## Requirements💻 :

Ensure you have the following dependencies installed:

- Python (version 3.9.x || 3.7.x)
- IDE: VS-CODE or collab
- Virtual-environment(venv)
- Other dependencies (refer to the requirement.txt)

You can install the required Python packages using:

```bash
pip install -r requirements.txt
```

## Setup 💿:

- Clone the repository:
```bash
git clone https://github.com/SINGHxTUSHAR/Cascading-Vision.git
cd Cascading-Vision
```
- Create a virtual environment (optional but recommended):
```bash
python -m venv venv
```
- Activate the virtual environment:
  - On Windows:
   ```bash
   venv\Scripts\activate
   ```
  - On macOS/Linux:
  ```bash
  source venv/bin/activate
  ```

## Contributing 📌:
If you'd like to contribute to this project, please follow the standard GitHub fork and pull request process. Contributions, issues, and feature requests are welcome!

## Suggestion 🚀: 
If you have any suggestions for me related to this project, feel free to contact me at tusharsinghrawat.delhi@gmail.com or <a href="https://www.linkedin.com/in/singhxtushar/">LinkedIn</a>.

## License 📝:
This project is licensed under the <a href="https://github.com/SINGHxTUSHAR/Cascading-Vision/blob/main/LICENSE">MIT License</a> - see the LICENSE file for details.
