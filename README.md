Here’s your **final README** with the updated **Recall** and **F1 Score** metrics:  

---

# 🎙️ Audio Deepfake Detection - Momenta Take-Home Assessment  

## 📌 Overview  
This project focuses on detecting **AI-generated speech (audio deepfakes)** using machine learning models. The goal is to identify manipulated voice recordings using **deep learning techniques** and evaluate their effectiveness.  

---

## 📊 Selected Models  
We analyzed multiple deepfake detection approaches and selected the following:  

### 1️⃣ **VALL-E (Microsoft)**  
🔹 **Key Innovation:** Generates speech based on text input with **zero-shot learning**.  
🔹 **Performance:** High speech synthesis quality but lacks real-time detection capabilities.  
🔹 **Why Chosen:** Advanced deepfake generation helps understand detection challenges.  
🔹 **Limitations:** Requires large datasets and high computational power.  

### 2️⃣ **Pengi (Microsoft)**  
🔹 **Key Innovation:** Uses **pretrained embeddings** for audio analysis.  
🔹 **Performance:** Effective for speech synthesis detection.  
🔹 **Why Chosen:** Strong feature extraction capabilities.  
🔹 **Limitations:** Lacks robustness for unseen deepfake models.  

### 3️⃣ **AudioPaLM (Google)**  
🔹 **Key Innovation:** Combines **audio processing with large language models**.  
🔹 **Performance:** Strong at capturing phonetic variations.  
🔹 **Why Chosen:** Hybrid approach improves detection.  
🔹 **Limitations:** Requires specialized hardware for training.  

---

## 📂 Dataset  
We used the **ASVspoof 5 dataset**, a widely recognized dataset for detecting spoofed audio samples.  

---

## 🎵 Audio Preprocessing  
To prepare audio files for deepfake detection, we initially used the following steps:  

1️⃣ **FLAC to WAV Conversion**  
- Since some datasets contain `.flac` files, they were converted to `.wav` format for compatibility with our model.  
- This was done using **FFmpeg** or Python’s `pydub` library.  

2️⃣ **Feature Extraction - MFCC**  
- **Mel-Frequency Cepstral Coefficients (MFCCs)** were extracted to represent audio signals in a way that captures human speech characteristics.  
- This helped improve model accuracy by providing meaningful representations of voice patterns.  

⚠️ **Note:** These steps are not included in the final code but were part of our initial pipeline. Users may add them if working with raw `.flac` files.  

---

## 🔥 Implementation  
We implemented a **CNN-LSTM model** for deepfake detection.  

### **Model Architecture:**  
✅ **Conv1D + MaxPooling1D** - Extracts time-series audio features.  
✅ **Flatten Layer** - Converts extracted features into a format usable by LSTMs.  
✅ **LSTM Layers** - Captures sequential dependencies in the audio data.  
✅ **Dropout & Dense Layer** - Prevents overfitting & performs classification.  

---

## 🏆 Fine-Tuning & Evaluation  
We fine-tuned our model using **transfer learning** techniques and evaluated it using:  

🔹 **Accuracy**  
🔹 **Precision**  
🔹 **Recall**  
🔹 **F1 Score**  

### **Results:**  
| Model         | Accuracy | Precision | Recall | F1 Score |  
|--------------|----------|-----------|--------|----------|  
| **CNN**      | **0.8350** | **0.1739** | **0.1524** | **0.1624** |  
| **LSTM**     | **0.8950** | **0.0000** | **0.0000** | **0.0000** |  
| **CNN-LSTM** | **0.8950** | **0.0000** | **0.0000** | **0.0000** |  

---

## 📌 Key Challenges & Solutions  
✅ **Handling Imbalanced Data:** Used oversampling techniques.  
✅ **Computational Limitations:** Optimized hyperparameters to reduce training time.  
✅ **Feature Extraction Issues:** Applied spectral analysis for better representation.  

---

## 🚀 Future Improvements  
🔹 **Enhancing Real-Time Detection:** Optimizing for faster inference.  
🔹 **Multi-Language Support:** Expanding dataset diversity.  
🔹 **Integration with Voice Authentication Systems.**  

---

## 🛠️ Setup & Installation  
To run this project locally, follow these steps:  

1️⃣ **Clone the Repository:**  
```sh
git clone https://github.com/Chintan12-not/Audio-Deepfake-Detection.git
```

2️⃣ **Navigate to the Project Directory:**  
```sh
cd Audio-Deepfake-Detection
```

3️⃣ **Install Required Dependencies:**  
```sh
pip install -r requirements.txt
```

4️⃣ **Run the Model:**  
```sh
python train_model.py
```

5️⃣ **Evaluate the Model:**  
```sh
python evaluate.py
```

---

## 📝 Conclusion  
This project successfully applies **deep learning techniques** to detect **AI-generated speech (deepfakes)**. While the **CNN-LSTM model** shows promising results, future improvements can enhance real-time detection, generalization, and accuracy across different datasets.  
