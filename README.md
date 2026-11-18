# Intelligent-Adaptive-DNA-Steganography

An intelligent adaptive image steganography framework using Deep Reinforcement Learning (PPO), DNA encoding, and adaptive LSB embedding for secure image data hiding.





\# Intelligent Adaptive DNA Encoding Using Deep Reinforcement Learning for Secure Image Steganography



\## 1. Project Overview



This project proposes an intelligent image steganography framework that integrates DNA-based encoding techniques with Deep Reinforcement Learning (DRL) to improve the security and adaptability of secret image transmission.



The framework uses a Proximal Policy Optimization (PPO)-based agent to make embedding decisions based on the characteristics of individual image blocks. It aims to balance embedding capacity and stego-image quality through adaptive Least Significant Bit (LSB) embedding.



Unlike conventional approaches that use a fixed number of LSBs, the proposed framework supports adaptive selection among 1-bit, 2-bit, and 3-bit embedding options.



\## 2. Problem Statement



Traditional image steganography techniques often use fixed embedding strategies that may introduce noticeable distortions or provide limited adaptability to different image regions.



This project investigates an adaptive approach in which Deep Reinforcement Learning guides embedding decisions according to image-block characteristics, while DNA encoding provides an additional layer of data representation.



The primary objective is to develop a framework that balances:



\- Image quality.

\- Embedding capacity.

\- Adaptive embedding decisions.

\- Secret information recovery.

\- Robustness under different noise conditions.



\## 3. Project Objectives



\- Develop an image steganography framework using DNA encoding and Deep Reinforcement Learning.

\- Extract meaningful features from individual cover-image blocks.

\- Use a PPO agent to make adaptive embedding decisions.

\- Dynamically select the LSB embedding depth instead of always using a fixed value.

\- Evaluate the quality of generated stego images.

\- Implement secret-data extraction and recovery.

\- Investigate the effect of noise on extraction performance.



\## 4. Proposed Methodology



The proposed framework follows the pipeline below:



\*\*Cover Image → Preprocessing → Block Division → Feature Extraction → PPO Agent → DNA Encoding → Adaptive LSB Embedding → Stego Image\*\*



\### 4.1 Image Preprocessing



The cover image is prepared for embedding and divided into smaller blocks.



\### 4.2 Block Division



The cover image is divided into non-overlapping 8 × 8 blocks.



For a 512 × 512 cover image, this produces 4096 individual blocks.



\### 4.3 Feature Extraction



Four features are extracted from each block:



\- Variance

\- Shannon Entropy

\- Canny Edge Density

\- GLCM Contrast



These features represent the characteristics of each image region and are used as inputs to the reinforcement learning agent.



\### 4.4 Deep Reinforcement Learning



A PPO-based reinforcement learning agent is used to make embedding decisions.



The agent considers the image-block state and selects actions related to DNA mapping, LSB depth, pixel location, and embedding decisions.



\### 4.5 DNA Encoding



Secret information is transformed into a DNA-related representation using eight DNA mapping rules.



The selected mapping rule is used during the encoding and embedding process.



\### 4.6 Adaptive LSB Embedding



The framework supports three embedding depths:



\- 1 LSB

\- 2 LSB

\- 3 LSB



The objective is to allow the agent to select an appropriate embedding depth rather than relying on a fixed 3-LSB strategy.



\### 4.7 Extraction and Recovery



The extraction process retrieves the embedded information from the stego image and reconstructs the secret image.



The framework also investigates recovery performance under noise conditions.



\## 5. Technologies Used



| Component | Technology |

|---|---|

| Programming Language | Python |

| Numerical Processing | NumPy |

| Data Processing | Pandas |

| Image Processing | OpenCV, Pillow |

| Image Feature Extraction | scikit-image |

| Reinforcement Learning | Stable-Baselines3 |

| RL Algorithm | PPO / MaskablePPO |

| RL Environment | Gymnasium |

| Deep Learning Framework | PyTorch |

| Visualization | Matplotlib |

| Development Environment | Jupyter Notebook |

| Version Control | Git and GitHub |



\## 6. Dataset Information



The project uses image datasets for cover-image and secret-image processing.



\### Cover Images

\- Dataset: DIV2K

\- Cover image dimensions: 512 × 512

\- Block dimensions: 8 × 8

\- Number of blocks per cover image: 4096



\### Secret Images



The implementation supports multiple secret-image dimensions:



| Secret Image Size | Payload (Bits) |

|---|---:|

| 64 × 64 | 32,768 |

| 128 × 128 | 131,072 |

| 256 × 256 | 524,288 |

| 512 × 512 | 2,097,152 |



\*\*Note:\*\* Dataset files are maintained locally and are not included in this repository. Users must obtain the datasets separately and configure their paths before execution.



\## 7. Evaluation Metrics



The framework considers the following evaluation metrics:



| Metric | Purpose |

|---|---|

| MSE | Measures pixel-level distortion |

| PSNR | Evaluates stego-image quality |

| SSIM | Measures structural similarity |

| BER | Measures bit error rate during recovery |

| Bit Accuracy | Measures the accuracy of extracted bits |

| Exact Recovery | Checks whether the secret image is reconstructed correctly |

| Extraction Performance | Evaluates recovery under different conditions |



\## 8. Project Structure



```text

Intelligent-Adaptive-DNA-Steganography/

│

├── notebooks/

│   └── DNA\_DRL\_Steganography\_Implementation.ipynb

│

├── src/

│   └── (Source code modules)

│

├── configs/

│   └── (Configuration files)

│

├── docs/

│   └── (Project documentation)

│

├── results/

│   └── (Selected experimental results)

│

├── requirements.txt

├── README.md

├── .gitignore

└── LICENSE

```



\## 9. Installation



\### Prerequisites



\- Python

\- Jupyter Notebook

\- Git

\- Required Python libraries



\### Step 1: Clone the Repository



```bash

git clone https://github.com/NandhanaSubhekshanan/Intelligent-Adaptive-DNA-Steganography.git

```



\### Step 2: Navigate to the Project



```bash

cd Intelligent-Adaptive-DNA-Steganography

```



\### Step 3: Create a Virtual Environment



```bash

python -m venv venv

```



Activate it on Windows:



```bash

venv\\Scripts\\activate

```



\### Step 4: Install Dependencies



```bash

pip install -r requirements.txt

```



\### Step 5: Launch Jupyter Notebook



```bash

jupyter notebook

```



Open the notebook inside the `notebooks` directory.



\*\*Note:\*\* Dependency compatibility, dataset paths, and execution instructions should be verified before attempting a fresh installation.



\## 10. Current Implementation Status



The repository currently contains the initial research implementation notebook and dependency information.



The project is being developed and evaluated incrementally. The following areas form part of the ongoing work:



\- Refinement of PPO-based embedding decisions.

\- Validation of adaptive LSB selection.

\- End-to-end embedding and extraction validation.

\- Evaluation under different noise conditions.

\- Experimental analysis across secret-image sizes.

\- Documentation and organization of reusable source modules.



Results and implementation status will be updated as the research progresses.



\## 11. Future Enhancements



\- Improve the adaptive embedding policy.

\- Strengthen extraction and recovery performance under noise.

\- Conduct comprehensive experimental evaluation.

\- Compare the proposed framework with existing steganography methods.

\- Organize the notebook implementation into reusable Python modules.

\- Improve reproducibility through configuration files and documentation.



\## 12. Research Context



\*\*Research Area:\*\* Network Systems and Security



\*\*Research Topic:\*\* Intelligent Adaptive DNA Encoding Using Deep Reinforcement Learning for Secure Image Steganography.



This repository is maintained as part of an M.Tech research project.



\## 13. License



This project is licensed under the MIT License. See the `LICENSE` file for details.



\## 14. Repository



GitHub: https://github.com/NandhanaSubhekshanan/Intelligent-Adaptive-DNA-Steganography



