👁️ EyeSpy: Interpretable Fundus Image Classification
EyeSpy is a deep learning pipeline for automated classification of fundus images, designed to assist in early diagnosis of retinal diseases. It integrates multi-modal features (RGB + wavelet transforms), interpretable CNN architectures, and visual diagnostics using Grad-CAM overlays. Built for reproducibility and scalability, EyeSpy is optimized for GPU training and parallel preprocessing. 
.

🚀 Features 
- Wavelet-based preprocessing for enhanced texture representation
- CNN & ResNet50 architectures with transfer learning
- Multi-modal input fusion (RGB + wavelet features)
- Grad-CAM visualization for model interpretability
- Automated annotation pipeline using Labelme/CVAT integration
- Parallel preprocessing with OpenMP-enabled C++ modules
- GPU-accelerated training on RTX 3050 hardware
- Robust error handling and reproducible experiment tracking

🧠 Model Pipeline
- Preprocessing
- Resize, normalize, and apply wavelet transforms
- Convert to multi-channel tensors (RGB + wavelet)
- Model Training
- Transfer learning with frozen/unfrozen layers
- Cross-validation and benchmarking on 4000-image dataset
- Interpretability
- Grad-CAM overlays for visual diagnostics
- Bounding box generation and overlay export


Grad-CAM visualizations reveal strong activation around optic disc and lesion regions, validating clinical relevance.


🛠️ Installation
git clone https://github.com/Sameekshashetty30/eyespy.git
cd eyespy
pip install -r requirements.txt
.
⚙️ Configuration
Edit configs/config.yaml to set:
- Dataset path
- Model architecture
- Training hyperparameters
- Visualization options

📌 Usage
python src/train.py --config configs/config.yaml
python src/gradcam.py --image data/test/img_001.png --model checkpoints/model.pth



🧪 Dataset
- Public fundus datasets (e.g., DRIVE, EyePACS, HRF)
- Custom annotations via Labelme and CVAT
- Supports .jpg, .png, and .tiff formats

📈 Performance Optimization
- OpenMP-enabled C++ preprocessing for wavelet transforms
- GPU benchmarking with PyTorch/TensorFlow
- Parallel data loading and augmentation

