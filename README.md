# Pan Card Tampering Detection

This project is a Flask web application that compares an uploaded image to an existing reference image to detect tampering. The application highlights differences between the two images and calculates a similarity score.

## Features

- Upload an image to compare against a reference image.
- Resize and save both the uploaded and reference images for processing.
- Use OpenCV and scikit-image to compare images and calculate a similarity score.
- Highlight differences between images by drawing bounding boxes around the altered regions.
- Display the similarity score on the homepage.

## Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/pan-card-tampering.git
   cd pan-card-tampering
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

3. Activate the virtual environment:

   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On Unix or MacOS:
     ```bash
     source venv/bin/activate
     ```

4. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

5. Ensure the following directories exist in the `app/static` directory:
   - `uploads`: For saving uploaded images.
   - `original`: Should contain the reference image (`image.jpg`).
   - `generated`: For saving output images (highlighted differences).

## Usage

1. Start the Flask application:
   ```bash
   python run.py
   ```

2. Open your web browser and navigate to `http://127.0.0.1:5000/`.

3. Upload an image to compare against the reference image.

4. View the similarity score and images with highlighted differences.

## Project Structure

```
pan-card-tampering/
├── app/
│   ├── __init__.py
│   ├── routes.py
│   ├── static/
│   │   ├── uploads/
│   │   ├── original/
│   │   └── generated/
│   └── templates/
│       └── index.html
├── run.py
├── requirements.txt
└── README.md
```

## Dependencies

- Flask
- OpenCV (`cv2`)
- Pillow (`PIL`)
- scikit-image
- imutils


