# Attendance-via-Face-identification
Real-time Face Recognition Attendance System built using Python, OpenCV, and the face_recognition library. The system detects and recognizes faces via a webcam, matches them against pre-encoded student images, and automatically logs attendance with timestamps into a CSV file.

Programming Language: Python

Key Features:
1. Real-time face detection and recognition using webcam input
2. Automatic attendance logging with date and time
3. Deep learning–based facial feature extraction (128-D embeddings)
4. Duplicate attendance prevention within a single session
5. Visual feedback for recognized and unrecognized faces
6. Configurable recognition threshold for accuracy tuning

Libraries & Frameworks:
1. OpenCV (real-time video processing)
2. face_recognition (facial encoding and matching)
3. dlib (CNN-based ResNet model for face embeddings)
4. NumPy, Pandas (data handling and storage)

How It Works: 
1. Student images are loaded from a local directory and converted into facial embeddings.
2. Each face is represented as a 128-dimensional vector using a deep learning ResNet model.
3. The webcam captures live video frames and detects faces in real time.
4. Detected faces are encoded and compared with stored embeddings using distance metrics.
5. If the distance is below a defined threshold, the face is recognized.
6. Attendance is marked once per session and saved to a CSV file with timestamps.
7. Unknown faces are highlighted separately on the video feed.

Output: 
1. Live webcam window with bounding boxes:
a. Green box: Recognized face (attendance marked)
b. Red box: Unknown face
2. CSV file containing:
a. Student Name
b. Timestamp of attendance
