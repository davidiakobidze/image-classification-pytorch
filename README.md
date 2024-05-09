## Installation

To run this project, you'll need Python 3. It's recommended to use a virtual environment to manage dependencies.

1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```

2. Navigate to the project directory:
   ```bash
   cd <project_directory>
   ```

3. Create a virtual environment:
   ```bash
   python3 -m venv venv
   ```

4. Activate the virtual environment:
    - On Windows:
      ```bash
      venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

5. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```


## Output Format

The output of the learning process should be in the form of .xml and .bin files, which are compatible with the OpenVINO
library.

## Data Preparation
1. Ensure that the training images are labeled and organized within the data directory as follows:


    ```
    data/data/images
    ├── 1
    ├── 2
    ├── 3
    ├── 4
    ├── 5
    ├── 6
    ├── 7
    └── 8
    ```

## Model Training

Run the `train_model.ipynb` notebook to obtain the PyTorch -> ONNX model.

## Export to OpenVINO

Export the ONNX model to an OpenVINO model using the following command:

`mo --input_model model.onnx`

## Model Usage

Use the generated `model.bin` and `model.xml` files in your OpenVINO applications.

