Federated Deep Learning for Privacy-Preserving Cervical Cytology Segmentation
 
Python 3.9+, TensorFlow 2.x / Keras, OpenCV (CLAHE), scikit-image, NumPy, 
Matplotlib, Seaborn — trained on Google Colab A100 GPU and Kaggle P100

July 2025 - May 2026

Phase 1 -
Designed a privacy-preserving federated learning framework for automated segmentation of nucleus and cytoplasm regions in 
cervical cytology images, addressing the real-world constraint that hospitals cannot share sensitive patient data. Distributed 
the Cx22 dataset across multiple simulated non-IID clients to emulate cross-institutional variability in staining and 
morphology. Benchmarked seven encoder-decoder architectures - ResUNet, MultiResUNet, DenseNet-UNet, MobileNet
UNet, Inception-UNet, EfficientNet-UNet, and ResUNet3+ under FedAvg aggregation. Evaluated six advanced loss functions 
including Focal, Tversky, HoverNet, and Exponential Logarithmic (ExpLog), finding ExpLog to be the strongest single-loss 
performer. Proposed a three-level hybrid loss combining ExpLog, FedProx regularisation, and Knowledge Distillation-guided 
consistency alignment, which achieved the best overall results: cytoplasm Dice = 0.9487 and IoU = 0.9024. ResUNet3+ with 
this hybrid loss was the final model, outperforming all baselines on both segmentation tasks while ensuring zero raw data 
exchange across federated clients.

Phase 2 - 
Deep Learning, Federated Learning
Extended single-dataset FL framework to a realistic multi-dataset setting using Cx22, CCEDD, and CNSeg distributed across 3, 
4 simulated clients representing institutions with distinct staining protocols and morphology. Benchmarked UNet, 
DenseNet121-UNet, and ResUNet3+ across 7 experiment configurations. Introduced Weighted FedAvg aggregation by client 
validation Dice score, CLAHE contrast normalization, KD ramp-up, cosine LR decay, TTA, and small object post-processing. 
ResUNet3+ with FedProx + KD achieved the best result — Dice = 0.823, IoU = 0.699.
 Implemented and compared advanced federated learning algorithms including FedAvg, FedProx, FedBN, FedDyn, FedProto, 
SCAFFOLD, Ditto, and FedNova on Cx22 dataset. Achieved robust privacy-aware medical image segmentation across Cx22, 
CCEDD, CNSeg, SIPaKMeD, and ISBI datasets while improving feature consistency and federated convergence.

