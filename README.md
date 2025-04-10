```markdown
# 🎯 Object Detection on Video using MobileNetSSD (Google Colab)

This project demonstrates how to perform real-time object detection on a video using the pre-trained **MobileNetSSD** model with OpenCV's DNN module in **Google Colab**.

It:
- Uses the MobileNetSSD model for object detection.
- Accepts a user-uploaded `.mp4` video.
- Processes each frame, draws bounding boxes and class labels.
- Saves the processed video with detections as an output file.
- Allows downloading the output from Colab.

---

## 📁 Files Included

| File                          | Purpose                                           |
|------------------------------|---------------------------------------------------|
| `MobileNetSSD_deploy.prototxt.txt` | Network architecture definition file             |
| `MobileNetSSD_deploy.caffemodel`  | Pre-trained model weights                        |
| `your_video.mp4`             | Input video file uploaded by user                |
| `output.avi`                 | Output video with object detection drawn         |
| `object_detection_colab.ipynb`     | Colab notebook containing full code             |

---

## 🔧 Requirements

Create a `requirements.txt` as below:

```
opencv-python
imutils
numpy
```

You don't need to manually install these in Google Colab — they come pre-installed. But the `requirements.txt` is useful if you want to run it locally or in a different environment.

---

## 🚀 How to Use (in Google Colab)

### 1. Upload Files
Upload the following to Colab using `files.upload()`:
- `MobileNetSSD_deploy.prototxt.txt`
- `MobileNetSSD_deploy.caffemodel`
- Your video file (`.mp4`, `.avi`, etc.)

### 2. Run Detection

The code:
- Loads the model.
- Reads the video frame-by-frame.
- Performs detection and annotates each frame.
- Saves it into `output.avi`.

### 3. Download Output

Once processed, download the video using:
```python
files.download("output.avi")
```

---

## 🎯 Model Details

**MobileNetSSD** is a lightweight object detection model trained on 20 object classes:
- `aeroplane`, `bicycle`, `bird`, `boat`, `bottle`, `bus`, `car`, `cat`, `chair`, `cow`, `diningtable`, `dog`, `horse`, `motorbike`, `person`, `pottedplant`, `sheep`, `sofa`, `train`, `tvmonitor`

The model outputs:
- Class label (e.g., "person")
- Confidence score (e.g., 98.5%)
- Bounding box (x, y, width, height)

---

## 📸 Sample Output

Detected objects are enclosed in bounding boxes and labeled, for example:

```
person: 96.47%
car: 89.02%
```

---

## 📌 Notes

- Only detections with confidence above `0.2` (20%) are shown.
- You can change this threshold in `args["confidence"]`.
- For longer videos, modify the `frame_count` condition to limit processing.

---

## 🧠 Credits

- Model: MobileNetSSD (Caffe format)
- Detection pipeline using OpenCV `cv2.dnn`
- Visualization using OpenCV + Google Colab's `IPython.display`

---

## 💬 Questions?

Feel free to raise issues or ask questions if anything’s unclear!
```

---

### ✅ `requirements.txt`

```
opencv-python==4.11.0.86
numpy>=1.21.2
imutils==0.5.4
```

---



Happy coding !!! 😊
