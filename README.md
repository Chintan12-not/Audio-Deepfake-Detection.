"# Audio Deepfake Detection" 
"# Audio Deepfake Detection" 
# 🎙️ Audio Deepfake Detection - Momenta Take-Home Assessment  

## 📌 Overview  
This project focuses on detecting **AI-generated speech** (audio deepfakes) using machine learning models. The goal is to identify manipulated voice recordings using deep learning techniques and evaluate their effectiveness.  

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
We used the **ASVspoof 5** dataset, a widely recognized dataset for detecting spoofed audio samples.  

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
We fine-tuned our model using transfer learning techniques and evaluated it using:  

🔹 **Accuracy**  
🔹 **Precision**  
🔹 **Recall**  
🔹 **F1 Score**  

**Results:**  
- **CNN Model:** Accuracy -  0.8350, Precision - 0.1739 
- **LSTM Model:** Accuracy - 0.8950, Precision - 0.0000 
- **CNN-LSTM Model:** Accuracy - 0.8950, Precision - 0.0000  

 

---

## 📌 Key Challenges & Solutions  
✅ **Handling Imbalanced Data:** Used oversampling techniques.  
✅ **Computational Limitations:** Optimized hyperparameters to reduce training time.  
✅ **Feature Extraction Issues:** Applied spectral analysis for better representation.  

---

## 🚀 Future Improvements  
- **Enhancing Real-Time Detection:** Optimizing for faster inference.  
- **Multi-Language Support:** Expanding dataset diversity.  
- **Integration with Voice Authentication Systems.**  

---

## 🛠️ Setup & Installation  
To run this project locally, follow these steps:  

1️⃣ **Clone the Repository:**  
```sh
git clone https://github.com/Chintan12-not/Audio-Deepfake-Detection.git
