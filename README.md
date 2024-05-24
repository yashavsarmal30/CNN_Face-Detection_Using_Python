# Simple Face Detection Project with Age and Gender Prediction Using Webcam Applications 📷

This project demonstrates a simple face detection system that uses a Convolutional Neural Network (CNN) pretrained model to detect faces in a video stream, and then predict the age and gender of the detected faces. The video stream is captured using a mobile phone camera as an external webcam.

## Features
- Detects faces in a video stream.
- Predicts the age and gender of detected faces.
- Uses a pretrained CNN model for face detection and age/gender prediction.
- Uses external camera rather than PC's default camera 📸 

## Prerequisites
- Python 3.11.1
- OpenCV
- Mobile phone (Android or iOS) to be used as an external webcam

## Setup Instructions

### Step 1: Install a Webcam App on Your Mobile Phone
1. **Android**: Install an app like [DroidCam](https://play.google.com/store/apps/details?id=com.dev47apps.droidcam) or [IP Webcam](https://play.google.com/store/apps/details?id=com.pas.webcam).
2. **iOS**: Install an app like [EpocCam](https://apps.apple.com/us/app/epoccam-webcamera-for-computer/id435355256) or [iVCam](https://apps.apple.com/us/app/ivcam-webcam/id1293057189).

### Step 2: Install the Corresponding Software on Your Computer
1. **DroidCam**:
   - Download and install the [DroidCam Client](https://www.dev47apps.com/droidcam/windows/) on your computer.
2. **IP Webcam**:
   - Access the video stream via a web browser or use third-party software like VLC to view the stream.
3. **EpocCam**:
   - Download and install the [EpocCam driver](https://www.elgato.com/en/epoccam) on your computer.
4. **iVCam**:
   - Download and install the [iVCam software](https://www.e2esoft.com/ivcam/) on your computer.

### Step 3: Connect Your Mobile Phone to Your Computer
1. **DroidCam**:
   - Open the DroidCam app on your mobile phone.
   - Open the DroidCam client on your computer.
   - Connect both devices using Wi-Fi or USB as per the instructions in the client.
2. **IP Webcam**:
   - Open the IP Webcam app on your mobile phone.
   - Start the server in the app and note the IP address and port displayed.
   - Open a web browser or VLC on your computer and enter the IP address and port (e.g., `http://192.168.1.2:8080`).
3. **EpocCam**:
   - Open the EpocCam app on your mobile phone.
   - Ensure both devices are on the same Wi-Fi network.
   - Open an application like Zoom or OBS on your computer and select EpocCam as the video source.
4. **iVCam**:
   - Open the iVCam app on your mobile phone.
   - Open the iVCam software on your computer.
   - Ensure both devices are on the same Wi-Fi network or connect via USB.

### Step 4: Modify Your Python Code to Use the Mobile Phone Camera Stream

#### For IP Webcam: 
In this tutorial we are using IP Webcam and the IP address of the mobile phone is `192.168.1.2` and the port is `8080` 
(You can use different webcam app of your choice) :
```python
.
.
.
# Replace the camera index with the URL of the IP Webcam stream or if you are using different app then read the corresponding documents 


video = cv2.VideoCapture("http://192.168.1.2:8080/video")
.
.
.
```

### Notes:
- Ensure your computer and mobile phone are on the same network.
- The URL used in `cv2.VideoCapture()` for IP Webcam should be the correct one displayed by the app.
- If using another app like DroidCam, refer to its documentation for the correct URL or device index.

By following these steps, you should be able to use your mobile phone as a webcam in your Python face detection script. This project leverages a CNN pretrained model to perform face detection and predict the age and gender of the detected faces, providing a simple yet effective solution for real-time video analysis.