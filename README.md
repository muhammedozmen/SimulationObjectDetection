# SimulationObjectDetection
Detection of cars, people, traffic lights in game with YOLO

## Installation

### 1_generate_dataset.ipynb
1 - Open your game that you want to perform detections
2 - In the game window, get the name of it's title bar
3 - Update the variable "window_name" with the game title bar name
4 - Run all cells to start generating your dataset in the folder images

### 2_label_dataset.ipynb
1 - Run the first 2 cells to declare the LabelUitls class
2 - Call the method create_shuffled_images_folder to shuffle the images generated in the previous notebook and insert them in a folder called shuffled_images
3 - Using the website makesense.ai, label the images from the shuffled_images folder
4 - After labeling the images, export the txt files with the labels from the website makesense.ai and copy the txt files into the shuffled_images folder
5 - Run the method create_labeled_images_zip_file to copy the labeled images to a zip file that will be used to train the model
6 - Update the classes variables with the label names that you used on makesense.ai
7 - Run the method update_config_files
8 - Upload the yolov4-tiny folder to the root of your google drive

### 3_yolo_model_training.ipynb
1 - Upload this notebook on Google Colab (this notebook need to run on Google Colab).
2 - Open the notebook on Google Colab.
3 - Change the Google Colab runtime to "GPU" by navigating to "Runtime" > "Change runtime type"
4 - Run all cells to start training your model.
5 - After the last command finish its execution, copy the file yolov4-tiny/training/yolov4-tiny-custom_last.weights from your google drive to the cloned project in the same folder as the 4_yolo_opencv_detector notebook.

### 4_yolo_opencv_detector.ipynb
1 - Open your game that you want to perform detections
2 - In the game window, get the name of it's title bar
3 - Update the variable "window_name" with the game title bar name
4 - Run all cells to start detecting objects using your trained model

## Features

- Detect the cars, people and traffic lights in the simulation (used GTA V as simulation)
- Shows us the name of objects after it detects
- Keeps the locations and names of objects as data


## Usage

### Click on Open Image button then choose an image that you want to upload and click on Scan QR Code or Scan Barcode button
![Click on Open Image button then choose an image that you want to upload and click on Scan QR Code or Scan Barcode button](/Screenshots/1.png?raw=true "Click on Open Image button then choose an image that you want to upload and click on Scan QR Code or Scan Barcode button")

### Here is the result of Barcode scan
![Here is the result of Barcode scan](/Screenshots/2.png?raw=true "Here is the result of Barcode scan")

### Here is the result of QR Code scan
![Here is the result of QR Code scan](/Screenshots/3.png?raw=true "Here is the result of QR Code scan")

