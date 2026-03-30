🎧 Audio Deepfake Detection (SceneFake + Fake-or-Real)
This project focuses on detecting fake vs real audio using deep learning, with special attention to a new threat scenario: manipulating the background acoustic scene while keeping the speaker’s voice and content unchanged.
The model is trained and evaluated using two datasets:

📌 Datasets Used
🎛️ SceneFake Audio Dataset
A dataset designed to address a neglected deepfake scenario, where attackers modify the background environment (scene) of real speech while keeping:
voice identity
linguistic content
prosody and timbre
The fake samples are generated using speech enhancement and audio scene manipulation techniques.

🗣️ Fake-or-Real Audio Dataset
A large dataset containing 170,000+ utterances of both real human speech and AI-generated speech.
Available versions include:
for-original: raw balanced dataset
for-norm: normalized sample rate, volume, and channels + balanced by gender/class
for-2sec: 2-second trimmed clips
for-rerec: rerecorded version simulating real voice channel playback

🚀 Model & Approach
This project uses the Audio Spectrogram Transformer (AST) from HuggingFace Transformers for audio classification.

Key Steps:
Audio preprocessing using torchaudio
Feature extraction using ASTFeatureExtractor
Training AST model for binary classification (Real vs Fake)
Evaluation using accuracy, confusion matrix, and classification report

🛠️ Technologies Used
Python
PyTorch & Torchaudio
HuggingFace Transformers (AST)
Scikit-learn
Pandas / NumPy
Matplotlib / Seaborn
📊 Output & Evaluation

The notebook provides:
training and validation performance
confusion matrix visualization
classification metrics (precision, recall, F1-score)

📌 Goal
The goal of this project is to build a robust deepfake detection system capable of identifying fake audio even when the manipulation is subtle, such as changing the background acoustic environment.
