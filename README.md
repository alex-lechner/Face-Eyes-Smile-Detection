# Face-Eyes-Smile Detection

[//]: # (References)
[no-smile]: ./imgs/screenshot-0.jpeg
[smile]: ./imgs/screenshot-1.jpeg
[opencv]: https://opencv.org/
[installation]: #installation-of-opencv
[haar-like-features]: https://www.quora.com/How-can-I-understand-Haar-like-feature-for-face-detection
[win-open-cv-wheel]: https://www.lfd.uci.edu/~gohlke/pythonlibs/#opencv

---

## Detection of faces, eyes, and smiles
This project uses [Haar-like features][haar-like-features] to detect faces, eyes, and smiles. It is done in Python 3.6 and uses the open source computer vision library [OpenCV][opencv]. To install OpenCV for Python please follow the [installation process below][installation].

By executing the script the internal webcam gets started and draws blue rectangles around faces, green rectangles around eyes and red rectangles around smiling mouths in the webcam video stream.

Face and eyes detection only       |  Face, eyes and smile detection
:---------------------------------:|:---------------------------------:
![no-smile][no-smile]              | ![smile][smile]

To start the face-eyes-smile detection clone this repository, open a terminal/command window and execute the following line in the root folder of this project:

```sh
python face_detection.py
```

If you don't have an internal webcam and you want to use an external webcam simply change the parameter of the `cv2.VideoCapture()` function on line 90 in `face_detection.py` from `0` to `1` like so:

```python
# 0 = internal webcam, 1 = external webcam
VIDEO_CAPTURE = cv2.VideoCapture(1)
```

In order to take a screenshot and save it into the `imgs` folder simply press the **`s`**-key on your keyboard*.

To close and exit the webcam video stream press the **`Esc`**-key on your keyboard*.

*while the window of your webcam video stream is active

## Installation of OpenCV
To install the OpenCV library for Python execute the following line in a terminal/command window:
```sh
pip install opencv-python
```

If you are on Windows and the line above does not work then download the OpenCV wheel from the [Unofficial Windows Binaries for Python Extension Packages Website][win-open-cv-wheel].

Because this project was done in Python 3.6 you need to download either `opencv_python‑3.4.3‑cp36‑cp36m‑win32.whl` for a 32-bit operating system or `opencv_python‑3.4.3‑cp36‑cp36m‑win_amd64.whl` for a 64-bit operating system. 

Note: `cp36` stands for the Python version 3.6 so if you are using Python 3.7 you will need to look for `cp37` in the filename.

After you have downloaded the proper file you need to navigate to the location where this file was downloaded (probably your Downloads-folder) and open the command window in this folder. Then execute the following line:
```sh
# Python 3.6 for 32-bit OS
pip install opencv_python‑3.4.3‑cp36‑cp36m‑win32.whl

# Python 3.6 for 64-bit OS
pip install opencv_python‑3.4.3‑cp36‑cp36m‑win_amd64.whl
```