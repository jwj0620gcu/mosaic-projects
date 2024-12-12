# Video Face Mosaic Program

This project uses Python and OpenCV to automatically detect faces in a video and apply mosaic effects to them. Users can input a video file path, and the program will generate a new video with mosaics applied to the detected faces.

---

## Features
- Automatically detects faces in the video.
- Applies mosaic effects to the detected faces.
- Saves the processed video as a new file.

---

## Requirements
### Required Libraries
- Python 3.x
- OpenCV

To install the required libraries, run the following commands:
```bash
pip install opencv-python
pip install opencv-python-headless
```

### Additional Requirements
- Haar Cascade file: The built-in OpenCV `haarcascade_frontalface_default.xml` file is used.

---

## Usage
1. **Run the Code**:
   Execute the following command in your terminal:
   ```bash
   python mosaic_video.py
   ```

2. **Input Video File Path**:
   After running, input the path to the video file. Example:
   ```
   Enter the path to the video for mosaic: example_video.mp4
   ```

3. **Check the Output**:
   - The processed video with mosaic effects will be saved as `mosaic_output.mp4`.

---

## Code Explanation
1. **Read Video**:
   The program reads the input video using `cv2.VideoCapture`.

2. **Face Detection**:
   Faces are detected using OpenCV's Haar Cascade classifier.

3. **Apply Mosaic**:
   Detected face areas are resized down and then upscaled to create a mosaic effect.

4. **Save Processed Frames**:
   The processed frames are saved to a new video file using `cv2.VideoWriter`.

5. **Resource Cleanup**:
   The program releases the video file and output resources after processing.

---

## Notes
- The input file path must be correct for the program to run successfully.
- If the Haar Cascade model fails to load, an error message will be displayed. Ensure OpenCV is installed properly.
- Performance may vary depending on the resolution and length of the video.

---

## Output Example
1. Run the program:
   ```bash
   python mosaic_video.py
   Enter the path to the video for mosaic: example_video.mp4
   ```

2. Output:
   ```
   The mosaicked video has been saved as 'mosaic_output.mp4'.
   ```

---

## Troubleshooting
- **Video cannot be opened**:
  - Ensure the input path is correct.
  - Verify that the video format is supported.

- **Face detection does not work**:
  - Poor lighting or obscured faces may affect detection.
  - Adjust `scaleFactor` and `minNeighbors` values to fine-tune detection.

- **Output video does not play**:
  - Ensure the `fps` value matches that of the input video.

---

## License
This project is licensed under the [MIT License](LICENSE).
