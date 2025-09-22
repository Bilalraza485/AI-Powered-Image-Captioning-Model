# 🖼️ Image Caption Generator

An advanced **Image Caption Generator** that automatically creates natural language descriptions for images using **Deep Learning**.  
This project combines **VGG16 (CNN)** for image feature extraction and a **Transformer-based Decoder** for text generation.  
It is designed to work with the **Flickr8k dataset**, focusing on images of living things.

---

## 🌟 Motivation

Understanding images and describing them in natural language is one of the most challenging tasks in AI.  
Image captioning combines **computer vision** (to “see”) and **natural language processing** (to “describe”).  
This project is part of my learning in Artificial Intelligence and aims to demonstrate how CNNs and Transformers can be integrated to produce meaningful captions.

---

## 📑 Project Highlights

- **Dataset:** Flickr8k (8,000 images + 5 captions each)
- **Feature Extractor:** Pre-trained VGG16 CNN
- **Caption Generator:** Transformer-based decoder
- **Focus:** Living things (animals, humans, nature scenes)
- **Goal:** Learn to bridge the gap between vision and language

---

## 🧠 How It Works

### 1️⃣ Data Collection
- Download the **Flickr8k dataset** which contains images and their respective captions.

### 2️⃣ Preprocessing
- Clean and normalize captions (lowercasing, removing punctuation, tokenizing).
- Create word-to-index and index-to-word dictionaries.
- Pad sequences to ensure uniform length.

### 3️⃣ Feature Extraction
- Use **VGG16** (pre-trained on ImageNet) to extract a 4096-dimensional feature vector for each image.
- Save these features for faster training.

### 4️⃣ Model Architecture
- **Encoder:** VGG16 CNN (fixed weights) extracts image features.
- **Decoder:** Transformer-based model that takes the image feature vector and generates a caption word by word.
- Uses attention mechanism to focus on relevant parts of the image.

### 5️⃣ Training
- Input: Image feature vector + previous words of the caption.
- Output: Next word in the caption.
- Optimizer: Adam
- Loss: Categorical cross-entropy.

### 6️⃣ Evaluation
- BLEU Score used to evaluate generated captions.
- Visual examples included for qualitative evaluation.

