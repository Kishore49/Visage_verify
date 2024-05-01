# Visage_verify


# Face Recognition Attendance System

This is a Flask web application for face recognition-based attendance tracking. The application allows users to register their faces,
take attendance using a webcam, and view attendance records.

## Installation

1. Clone the repository:

  

2. Install dependencies:

   pip install -r requirements.txt

3. Download the pre-trained face detection model:

   - Download the `haarcascade_frontalface_default.xml` file from [here](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml).
   - Place the downloaded file in the project directory.

4. Run the Flask app:

   python app.py

5. Access the app in your web browser at `http://localhost:5000`.

## Usage

- **Home Page**: View attendance records and take attendance.
- **List Users**: View and manage registered users.
- **Add User**: Register a new user by capturing their face images.
- **Delete User**: Remove a user from the system.

## Libraries Used

- **Flask**: Used for creating the web application.
- **OpenCV**: Used for face detection and image processing.
- **NumPy**: Used for numerical operations on arrays.
- **scikit-learn**: Used for training and using the K-Nearest Neighbors classifier for face recognition.
- **pandas**: Used for reading and writing CSV files for attendance records.
- **joblib**: Used for saving and loading the trained face recognition model.

## Implementation Details

1. **Face Detection**: OpenCV's `CascadeClassifier` is used to detect faces in images.
2. **Face Recognition Model**: A K-Nearest Neighbors classifier from scikit-learn is trained on the face images of registered users to recognize faces.
3. **Webcam Integration**: The app captures frames from the webcam, detects faces, and uses the trained model to recognize and mark attendance.
4. **Web Interface**: Flask renders HTML templates for displaying attendance records, user lists, and forms for adding/deleting users.
