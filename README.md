# Face-and-Emotion-Detection
Face and Emotion Detection Using Kalman Filter and Faceboxes

## Configure Settings
Edit settings in config.py
- I/O Setting
```python
self.VID_NAME = 'demo.mp4' # Input Video
self.VID_SAVING_NAME = 'save_video01.avi' # Output Video
self.VID_SAVING_BLOB_NAME = 'VID_SAVING_BLOB_NAME01.avi' # Output BLOB Video
```
- Tracking System Settings
```python
self.detector = ["kcf", "kalman"][1] # "kcf" for higher accuracy, "kalman" for quick detection
```

## Usage
Run traffic_main.py
```python
python -traffic_main.py
```

## Sample Output
[Sample](https://github.com/YanZhu1105/Face-and-Emotion-Detection/blob/master/save_video01.avi)

## Catch
The default OS for this repo is Windows. For some reason, OpenCV seems to only support AVI format video. If using Linux, in video_helper.py, use
```python
fourcc = cv2.VideoWriter_fourcc(*'MJPG')
```
instead of
```python
fourcc = cv2.VideoWriter_fourcc(*'DIVX')
```
