# AfroRacer

AfroRacer is an autonomous driving project designed to simulate a self-driving car using a robot car platform. The project leverages gamepad control for data collection, computer vision for image processing, and deep learning for driving behavior prediction. This repository contains all the necessary code, data, and models to train and test the autonomous driving system.

## Features

- **Gamepad-Controlled Data Collection**: Drive the robot car using a gamepad while recording images, steering, and throttle inputs.
- **Data Visualization**: Visualize driving scenarios and inspect the collected data.
- **Deep Learning Model**: Train a neural network (DriveNet) to predict steering and throttle commands based on input images.
- **Real-Time Testing**: Test the trained model on new images to evaluate its performance.
- **Model Saving**: Save the trained model for future use.

## Project Structure

```
AfroRacer/
├── data_logs/          # Directory for storing collected data and logs
│   └── log.csv         # CSV file containing image filenames, steering, and throttle data
├── src/                # Source code directory
│   ├── AfroRacer.ipynb # Jupyter Notebook for the entire project workflow
│   ├── drive_model.pth # Trained model file
│   └── data_logs/      # Duplicate data_logs directory (if applicable)
│       └── log.csv     # Duplicate log.csv file
```

## Workflow

### Step 0: Imports
Install the required libraries and import necessary modules.

### Step 0: Data Collection
Use a gamepad to drive the robot car while recording images, steering, and throttle inputs. The data is saved in the `data_logs/` directory.

### Step 1: Settings
Define project settings such as data paths, image dimensions, and training parameters.

### Step 2: Load & Preview Data
Load the collected data from the CSV file and preview it to ensure correctness.

### Step 3: Visualize Driving Scenarios
Visualize the driving scenarios by displaying the collected images along with their corresponding steering and throttle values.

### Step 4: Dataset Class
Define a custom PyTorch dataset class to handle image loading and preprocessing.

### Step 5: Transforms + DataLoader
Apply data transformations and create a DataLoader for efficient batch processing during training.

### Step 6: Define DriveNet
Implement the DriveNet neural network architecture for predicting steering and throttle commands.

### Step 7: Train Model
Train the DriveNet model using the collected data and visualize the training loss.

### Step 8: Plot Training Loss
Plot the training loss to monitor the model's performance over epochs.

### Step 9: Test Prediction
Test the trained model on new images to evaluate its predictions for steering and throttle.

### Step 10: Save Model
Save the trained model to a file for future use.

## Requirements

- Python 3.8+
- Jupyter Notebook
- PyTorch
- OpenCV
- pygame
- matplotlib
- pandas
- numpy

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/AfroRacer.git
   cd AfroRacer
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the Jupyter Notebook:
   ```bash
   jupyter notebook src/AfroRacer.ipynb
   ```

## Usage

1. Connect a gamepad to your computer.
2. Run the notebook and follow the steps sequentially.
3. Use the gamepad to collect data in Step 0.
4. Train the model using the collected data.
5. Test the model on new images to evaluate its performance.

## Contributing

Contributions are welcome! If you have ideas for improving AfroRacer, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- Inspired by self-driving car projects and the open-source community.
- Special thanks to contributors and testers for their valuable feedback.