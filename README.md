# Webcam Heart Rate Monitor
Measure Your Heart Rate Using Your Webcam!

*Note: This project was made for educational purposes only. This is not for commercial use. The algorithm is based on the incredible work done at the MIT Computer Science & Artificial Intelligence Lab. Please check out their [work](http://people.csail.mit.edu/mrub/evm/).*

This project can monitor a user's heart rate in real time using just a webcam. It is a PPG ([Photoplethysmogram](https://en.wikipedia.org/wiki/Photoplethysmogram)) solution based on a color magnification [algorithm](http://people.csail.mit.edu/mrub/papers/vidmag.pdf) which makes it possible to see the color of your face change as blood rushes in and out of your head. This project allows you to visualize your face as it pulsates in real time. Since it is able to detect your pulses, it also calculates your heart rate in beats per minute (BPM). 

![Demo Gif](https://media.giphy.com/media/idMIx2UeRIA8Kb2YAz/giphy.gif)

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing.

### Prerequisites
Ensure the computer you are using to run this project has a webcam. 

These are the library versions I am using (other versions haven't been tested):
```
python 2.7.13
numpy  1.13.1
opencv 2.4.11
```

### Installing

Install python [here](https://www.python.org/download/releases/2.7.3/)

Install numpy: `pip install numpy`

Install opencv2 on MacOS: `brew install opencv@2`. *Check out [Homebrew](https://brew.sh), the package manager for MacOS.*


Use the following commands in the terminal to check the library versions installed:
```
python --version
python -c "import numpy; print numpy.__version__"
python -c "import cv2; print cv2.__version__"
```

### Usage

Once the project is downloaded. Run the python file:

```
python main.py
```

The webcam light should activate and there should be a small window that appears. The program takes a few seconds to detect the pulse and start calculating your heart rate so be patient. While the program is running, it saves the original unmodified webcam video as 'original.mov' as well as a video of the output called 'output.mov'. Both of these videos will be overwritten every time the program is run, so make sure to copy the videos you would like to save to another directory.

To quit the program press 'q' on your keyboard.


If you would like this program to analyze a video, instead of the real time webcam, simply pass the location of the video as a parameter. The program will generate an output based on the provided video. The input video must be 320x240. Here is an example:
```
python main.py original.mov
```

### Tips for Best Results

- Make sure your face is well lit

- Place your forehead in the green box (area of detection)

- Try not to move or blink too much

