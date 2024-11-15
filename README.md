# Quantum Neural Networks for Brain Image Analysis
**Intel Student Ambassador Fall Hackathon 2024 Project**

This project explores the use of Quantum Neural Networks (QNNs) for brain image analysis, leveraging Intel hardware optimizations to improve performance and efficiency. The project focuses on using Intel Gaudi (HPU) and the Intel Extension for PyTorch, along with the OpenVINO Toolkit.

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Model Optimization](#model-optimization)
- [Results](#results)
- [Experiments: Trial and Error](#experiments-trial-and-error)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to analyze brain images using Quantum Neural Networks (QNNs). We aim to leverage Intel optimizations to improve the performance of the neural network models.

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
pip install intel-extension-for-pytorch openvino
pip install torchquantum
pip install qiskit==0.43.1 qiskit-terra==0.24.1 qiskit-aer==0.12.0 qiskit-ibm-provider==0.6.1 qiskit-ibm-runtime==0.10.0
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
   . QuantumSegnets.ipynb
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

## Experiments: Trial and Error

"The beauty of science is to be productively wrong."

This project involved numerous experiments, reflecting the iterative nature of scientific research. Below are some of the challenges we faced and how we approached them:

- **Intel Tiber Instance**: During one of our experiments, our instance on Intel Tiber crashed. Despite multiple discussions with the Intel team, we couldn't get it back up and running in time. At this point, we had already completed some inferencing with OpenVINO. After consulatation with our Mentor Ugonna, we found an alternative to run the code on the Intel Tiber using the notebooks on the learn section. Doing so we were able to run and test our code on Gaudi successfully.

- **Inference and Optimization**: After successfully running the model locally, we optimised the code for compatibility with Intel hardware (Gaudi) and further refined it using Intel software dependencies. Fortunately, we were able to test the updated code on Intel Tiber by making use of the notebooks on Intels Learn platform which proved to be more than a platform for just eduction.

![Unknown](https://github.com/user-attachments/assets/0e2a3959-efb4-40dc-add6-540cdbe30b4d)

## Contributing
We welcome contributions! Please create a pull request or open an issue if you have suggestions.

