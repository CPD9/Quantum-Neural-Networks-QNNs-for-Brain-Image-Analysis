# Quantum Neural Networks for Brain Image Analysis
**Intel Student Ambassador Fall Hackathon 2024 Project**

# Quantum Neural Networks (QNNs) for Brain Image Analysis

This project explores the use of Quantum Neural Networks (QNNs) for brain image analysis, leveraging Intel hardware optimizations to improve performance and efficiency. The project focuses on using Intel Gaudi (HPU) and the Intel Extension for PyTorch, along with the OpenVINO Toolkit.

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Model Optimization](#model-optimization)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to analyze brain images using Quantum Neural Networks (QNNs). We aim to leverage Intel optimizations and a quantum layer to improve the performance of the neural network models.

<img width="805" alt="Screenshot 2024-11-14 at 02 41 51" src="https://github.com/user-attachments/assets/b4591cd6-1817-4561-a8d6-a1a011c11b65">


## Installation

### Step 1: Set Up a Virtual Environment
We recommend using a virtual environment to manage dependencies:

```bash
python -m venv qnn-env
source qnn-env/bin/activate  # On Windows use `qnn-env\Scripts\activate`
```

### Step 2: Install Required Dependencies
Install the necessary packages using the following commands:

```bash
pip install numpy opencv-python matplotlib torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install intel-extension-for-pytorch openvino habana-torch
```

### Step 3: Verify Installation
Ensure all packages are installed correctly:

```bash
pip list
```

## Usage
To run the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/CPD9/Quantum-Neural-Networks-QNNs-for-Brain-Image-Analysis.git
   cd Quantum-Neural-Networks-QNNs-for-Brain-Image-Analysis
   ```

2. Activate your virtual environment:
   ```bash
   source qnn-env/bin/activate
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook QuantumSegnet.ipynb
   ```

## Model Optimization
This project uses Intel optimizations for better performance:

- **Intel Extension for PyTorch**:
  ```python
  import intel_extension_for_pytorch as ipex
  model = ipex.optimize(model)
  ```

- **OpenVINO Inference**:
  ```python
  from openvino.runtime import Core

  def load_openvino_model(model_path):
      ie = Core()
      model = ie.read_model(model=model_path)
      compiled_model = ie.compile_model(model=model, device_name="CPU")
      return compiled_model
  ```

## Results
The project includes performance benchmarks demonstrating the improvements when using Intel optimizations.

<img width="1212" alt="Screenshot 2024-11-14 at 02 38 54" src="https://github.com/user-attachments/assets/015fafc4-be81-4f95-bc1f-484c28966d2f">

<img width="1238" alt="Screenshot 2024-11-14 at 02 39 10" src="https://github.com/user-attachments/assets/e4eb7180-f9e7-44ea-b313-0ec58e281a13">


## Contributing
We welcome contributions! Please create a pull request or open an issue if you have suggestions.

## License
This project is licensed under the MIT License.
