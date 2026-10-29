# MediaPipe Computer Vision Demos

A collection of small Python experiments using [MediaPipe](https://mediapipe.google.dev/) and OpenCV. The scripts demonstrate real-time face, hand, pose, and object tracking, along with face-mesh effects. Each script is an independent example; there is no single application entry point.

## Demos

| Script | What it demonstrates |
| --- | --- |
| `3D_Face_Transform.py` | Face mesh, contours, and iris landmarks from a webcam. |
| `3D_Face_Transform_2face.py` | Face replacement/compositing experiment using a video source. The source path is currently hard-coded in the script. |
| `3D_Face_Transform_colorchange.py` | Face-mesh color-change effect. |
| `3D_Face_Transform_with_Shadow.py` | Face-mesh effect with a shadow treatment. |
| `3D_object_detection.py` | 3D object detection demo. |
| `3D_object_detection_with_video.py` | 3D object detection using video input. |
| `FaceHand_Landmark_Detection.py` | Face and hand landmark detection. |
| `Hand_Landmark_Detection.py` | Hand landmark detection. |
| `Instant_Motion_Tracking.py` | Real-time motion tracking. |
| `Object_Detection_with_WebCam.py` | Object detection from a webcam. |
| `Pose_Landmark_Detection.py` | Pose landmark detection. |
| `Real_time_Body_Pose.py` | Real-time body pose tracking. |
| `Realtime_pose_tracking_with_video.py` | Pose tracking on video input. |

## Requirements

- Python 3
- A working webcam for webcam-based examples, or a video file for video-based examples
- Python packages used by the examples: `mediapipe`, `opencv-python`, and, for compositing examples, `numpy`

Install the common packages in a virtual environment:

```bash
python -m venv .venv
```

Activate it, then install the packages:

```bash
# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate

python -m pip install mediapipe opencv-python numpy
```

MediaPipe APIs and supported Python versions vary by release. If a script reports an import or API error, check the MediaPipe version expected by that example and install a compatible version.

## Run an example

Clone the repository, change into its directory, and run one script at a time:

```bash
git clone https://github.com/dhilleswar07/Mediapipe.git
cd Mediapipe
python Hand_Landmark_Detection.py
```

Replace the script name with another demo from the table. Webcam examples typically open camera index `0`; change the `cv2.VideoCapture(...)` value in a script if your camera uses another index. For video examples, update the video path in the script to a file on your computer. Press **Q** in the OpenCV preview window to quit when that control is present.

## Notes

- These are learning examples, not a unified package. Their options, input handling, and MediaPipe APIs may differ.
- Some scripts may contain machine-specific file paths. Update those paths before running the example on another computer.
- Camera access must be enabled for the terminal or application running Python.

## License

No license is specified in the repository. Contact the author before redistributing or using the code in a way that requires reuse rights.
