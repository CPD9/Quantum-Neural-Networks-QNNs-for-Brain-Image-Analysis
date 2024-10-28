# Quantum Neural Networks for Brain Image Analysis
**Intel Student Ambassador Fall Hackathon 2024 Project**

## Project Overview
This project explores the potential of Quantum Neural Networks (QNNs) for brain image analysis, aiming to improve diagnostic accuracy and speed in medical imaging. Leveraging Intel’s advanced AI and quantum tools—including **Intel Tiber™ AI Cloud**, **OpenVINO™ Toolkit**, and **Intel Quantum SDK**—we integrated quantum layers into a traditional neural network, resulting in a hybrid model optimized for real-time medical diagnostics.

## Problem Statement
In medical imaging, accurately analyzing brain scans is crucial for detecting conditions like tumors, strokes, and degenerative diseases. However, traditional models often struggle with the complexity and high-dimensionality of brain imaging data, resulting in processing delays and potential diagnostic inaccuracies. Our project addresses this by using quantum-enhanced neural networks to optimize both feature extraction and inference speed.

## Solution
We developed a Quantum Neural Network (QNN) that combines classical neural networks with quantum layers to create a hybrid architecture. This approach enhances feature extraction, helping to identify subtle patterns in brain images that may otherwise go undetected. The model was optimized and deployed using Intel’s tools to ensure high performance and compatibility with various environments.

## Technologies Used
- **Intel Tiber™ AI Cloud**: Provided scalable virtual machine infrastructure for model training and testing.
- **OpenVINO™ Toolkit**: Enabled us to optimize the model for faster inference and real-time processing. The toolkit converted our PyTorch models to ONNX and optimized them for Intel hardware, ensuring compatibility across CPUs, GPUs, and VPUs.
- **Intel Quantum SDK**: Allowed us to integrate quantum layers within the neural network, enabling enhanced feature extraction and quantum-level processing capabilities.

## Team Members
- **Peter Dike** - Product Manager, Austria
- **Sreeneha Samudrala Snighdha** - Data Scientist, Austria
- **Nwankwo Chijioke** - Front-end Developer, Chicago
- **Mentor**: Ugonna (Intel Student Program Mentor)

## Project Workflow
1. **Data Preparation**: Processed brain imaging data to ensure consistency and high quality for training and validation.
2. **Model Development**:
   - Integrated quantum layers using Intel Quantum SDK for enhanced feature extraction.
   - Optimized model layers with OpenVINO for performance across Intel hardware.
3. **Testing & Evaluation**:
   - Conducted comparative testing between our Quantum Model and a traditional SegNet model.
   - Evaluated using Intersection over Union (IOU) and Binary Cross-Entropy (BCE) loss metrics to determine effectiveness.
4. **Deployment**:
   - Deployed on Intel Tiber™ AI Cloud for efficient resource management and scalable access.
   - Optimized for multi-platform compatibility using OpenVINO.

## Results
- **SegNet Layer**:
  - Mean Train IOU: 81.6%
  - Mean Test IOU: 82.5%
- **Quantum Model**:
  - Mean Train IOU: 81.3%
  - Mean Test IOU: 80.5%

Although our Quantum Model showed slightly lower IOU metrics initially, its advanced feature extraction capabilities highlight its potential. With further refinement, the quantum-enhanced model could surpass traditional architectures in both speed and accuracy.

## Getting Started
### Prerequisites
1. Python 3.x
2. Intel Quantum SDK
3. OpenVINO Toolkit
4. PyTorch and ONNX

### Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/QuantumNeuralNetwork-BrainImageAnalysis.git
   cd QuantumNeuralNetwork-BrainImageAnalysis
   
### Set up Virtual Environment
```bash
python -m venv qnn-env
source qnn-env/bin/activate   # For MacOS/Linux
qnn-env\Scripts\activate      # For Windows
