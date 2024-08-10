# Cat and Dog Image Classifier

This project is a simple deep learning model built using TensorFlow and Keras to classify images of cats and dogs. The project includes data preprocessing, model training, and evaluation using TensorBoard for visualization.

## Project Structure

```
.
|   .gitignore
|   app.py
|   cat_test.jpeg
|   dog_test.jpg
|   model.ipynb
|   README.md
|
+---data
+---logs
|   +---train
|   |       events.out.tfevents.1709553200.NOOR.26464.0.v2
|   |       events.out.tfevents.1709554017.NOOR.26464.2.v2
|   |       events.out.tfevents.1709554339.NOOR.18896.0.v2
|   |
|   \---validation
|           events.out.tfevents.1709553206.NOOR.26464.1.v2
|           events.out.tfevents.1709554023.NOOR.26464.3.v2
|           events.out.tfevents.1709554344.NOOR.18896.1.v2
|
\---models
        catdogmodel.h5
```

## Requirements

- Python 3.x
- TensorFlow
- OpenCV
- NumPy
- Matplotlib

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/cat-dog-image-classifier.git
   cd cat-dog-image-classifier
   ```

2. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Ensure you have the `data` directory with subdirectories for training and validation images of cats and dogs.

## Model Training

The model is defined and trained in the `model.ipynb` notebook. The training includes data preprocessing steps such as image scaling and removing corrupted images.

### Steps:

1. **Data Loading and Preprocessing:**

   - Images are loaded from the `data` directory.
   - Images are validated and corrupted images are removed.
   - Data is split into training, validation, and test sets.
   - Images are scaled to a range of 0 to 1.

2. **Model Definition:**

   - A sequential CNN model is defined with Conv2D, MaxPooling2D, Dense, and Flatten layers.
   - The model uses 'relu' activation for hidden layers and 'sigmoid' for the output layer.

3. **Model Training:**

   - The model is compiled with the Adam optimizer and binary cross-entropy loss.
   - TensorBoard and EarlyStopping callbacks are used.
   - The model is trained for up to 40 epochs with early stopping based on validation loss.

4. **Model Evaluation:**

   - Training and validation accuracy and loss are monitored.
   - TensorBoard is used for visualization of training progress.

## Running the Model

You can test the trained model with new images by running `app.py`.

## TensorBoard Visualization

Logs for TensorBoard are saved in the `logs` directory. To visualize the training process, run:

```bash
tensorboard --logdir=logs
```

Open the provided URL in a web browser to view the training and validation metrics.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

This project uses TensorFlow and Keras for deep learning and OpenCV for image preprocessing. Special thanks to the TensorFlow community for their excellent documentation and support.

This is a project for the Bharat internship tasks 2nd task is Image Classifier
