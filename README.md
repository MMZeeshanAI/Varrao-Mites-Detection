# Varroa Mites Detection

This project focuses on using Convolutional Neural Networks (CNN) to detect and count Varroa mites on a white piece of cardboard or plastic, which helps assess hive health status (healthy, moderately healthy, or dying). The results are served via a web app, allowing users to upload images and receive mite counts along with hive health feedback.

## Features

- **Automated Varroa Mite Detection**: Identify and count the number of Varroa mites in images using a trained CNN.
- **Health Status Classification**: Convert mite counts into hive health status categories.
- **Web App Integration**: The detection system is deployed as a web app using Uvicorn.

## Prerequisites

Ensure the following prerequisites are installed on your system:

- **Python 3.6+**: This project requires Python 3.6 or higher.
- **pip**: Python's package installer, used to install project dependencies.

## Setup Instructions

### 1. Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/MMZeeshanAI/Varroa-Mites-Detection.git
cd Varroa-Mites-Detection
```

### 2. Create a Virtual Environment

It is recommended to use a virtual environment to manage dependencies. Run the following commands to create and activate a virtual environment:

#### For macOS and Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

#### For Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

Once the virtual environment is activated, install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### 1. Start the Web App

To start the web app, use Uvicorn to run the server:

```bash
uvicorn app:main --reload
```

This will launch the web app on `http://127.0.0.1:8000`, where you can upload images for Varroa mite detection.

### 2. Detecting Varroa Mites

Once the web app is running, navigate to the provided URL in your browser and upload an image. The web app will display the number of detected mites and the corresponding hive health status.

## Project Structure

- `train.py`: Script for training the CNN model.
- `app.py`: Script containing the web app built with FastAPI.
- `models/`: Directory containing the trained model weights.
- `data/`: Directory for storing the training and test datasets.
- `templates/`: Contains HTML templates for the web interface.

## Contributions

Contributions are welcome! Please feel free to submit a pull request or report any issues.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
