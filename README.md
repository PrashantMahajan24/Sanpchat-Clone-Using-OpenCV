# Snapchat Clone for Photo Filters

A simple **Snapchat-style face filter project** built using **Python and OpenCV**.
The project detects faces and eyes from images or webcam frames and applies different photo filters and face effects.

## Features

* Face detection using Haar Cascade
* Eye detection using Haar Cascade
* Grayscale filter
* Sepia filter
* Vintage filter
* Warm and cool effects
* Vignette effect
* Invert filter
* Colour pop effect
* Cartoon filter
* Beauty / skin-smoothing filter
* Dog ears and nose filter
* Sunglasses filter
* Moustache filter
* Bunny ears filter
* Party crown filter
* Big-eyes filter
* Real-time webcam filters
* Save filtered webcam snapshots

## Technologies Used

* Python
* OpenCV
* NumPy
* Matplotlib
* Haar Cascade Classifier

## How It Works

1. Load an image or use the webcam.
2. Detect the face using OpenCV Haar Cascade.
3. Detect the eyes inside the detected face region.
4. Apply the selected filter or face effect.
5. Display the processed image.
6. In webcam mode, the filter is applied in real time.

## Project Workflow

```text
Input Image / Webcam
        ↓
Face Detection
        ↓
Eye Detection
        ↓
Select Filter
        ↓
Image Processing
        ↓
Filtered Image / Live Output
```

## Available Filters

| Filter     | Description                                                   |
| ---------- | ------------------------------------------------------------- |
| Grayscale  | Converts the image to grayscale                               |
| Sepia      | Gives the image a classic brownish effect                     |
| Vintage    | Combines sepia, vignette, fading and noise                    |
| Warm       | Increases warm/red tones                                      |
| Cool       | Increases cool/blue tones                                     |
| Vignette   | Darkens the edges of the image                                |
| Invert     | Inverts image colors                                          |
| Colour Pop | Keeps the detected face in color and makes the rest grayscale |
| Cartoon    | Creates a cartoon-style effect                                |
| Beauty     | Smooths the detected face area                                |
| Dog        | Adds dog ears and nose                                        |
| Sunglasses | Adds sunglasses around the detected eyes                      |
| Moustache  | Adds a moustache to the face                                  |
| Bunny      | Adds bunny ears                                               |
| Crown      | Adds a party crown                                            |
| Big Eyes   | Enlarges the detected eye regions                             |

## Installation

Install the required Python libraries:

```bash
pip install opencv-contrib-python==4.10.0.84 numpy matplotlib
```

## Running the Project

### 1. Run the Notebook

Open the notebook in Jupyter Notebook, JupyterLab, or Google Colab.

Run the cells in order.

### 2. Use Your Own Image

The notebook checks for a local image and uses a generated cartoon face as a fallback when the image is not available.

Update the image path in the notebook:

```python
photo = cv2.imread("your_image_path.jpg")
```

### 3. Run Webcam Filters

The project includes a real-time webcam function:

```python
live_filter_webcam()
```

The webcam version is designed to run in a **local Python environment with a connected webcam and display**.

## Webcam Controls

| Key | Filter        |
| --- | ------------- |
| `0` | None          |
| `1` | Grayscale     |
| `2` | Sepia         |
| `3` | Vintage       |
| `4` | Cartoon       |
| `5` | Beauty        |
| `6` | Dog           |
| `7` | Sunglasses    |
| `8` | Moustache     |
| `9` | Bunny         |
| `c` | Crown         |
| `b` | Big Eyes      |
| `s` | Save Snapshot |
| `q` | Quit          |

When a snapshot is saved, it is stored with a filename such as:

```text
snapshot_dog.png
```

## Face Detection

The project uses OpenCV's Haar Cascade classifiers:

```python
haarcascade_frontalface_default.xml
haarcascade_eye.xml
```

The largest detected face is selected as the main face. Eye detection is performed inside the detected face region to reduce false detections.

## Project Structure

```text
Snapchat-Clone/
│
├── Sanpchat.ipynb
└── README.md
```

## Important Note

The notebook contains a local image path for testing and a fallback cartoon face. For GitHub, avoid uploading personal photos or other private files.

The webcam functionality should be run in a local Python environment because webcam/display access may not work directly in all notebook environments.

## Future Improvements

* Add more Snapchat-style filters
* Add a graphical user interface
* Add filter selection buttons
* Improve face tracking
* Add multiple-face support
* Add video recording
* Add image download/save options
* Improve filter positioning for different face angles

