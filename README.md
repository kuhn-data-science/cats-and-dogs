# Cats vs. Dogs – CNN Image Classification

A convolutional neural network (CNN) that classifies images of **cats** and **dogs** using the **Oxford-IIIT Pet Dataset**.  
Focus: how **cropping**, **class balancing**, and **preprocessing** impact model accuracy and generalization.

---

## 📊 Project Overview
- **Dataset:** Oxford-IIIT Pet Dataset (N = 14.005)  
- **Classes:** Cat 🐱 / Dog 🐶  
- **Splits:** Train 12.899 | Val 738 | Test 368  
- **Image Size:** 128×128 px (originally 640×640)  
- **Source:** [Roboflow Universe – Oxford Pets](https://universe.roboflow.com/brad-dwyer/oxford-pets)

---

## ⚙️ Model Setup
- **Architecture:** 2×Conv2D → MaxPooling → Dense(128) + Dropout(0.3) → Sigmoid  
- **Optimizer:** Adam (lr=0.0001)  
- **Loss:** Binary Crossentropy  
- **Epochs:** 10  
- **Tools:** TensorFlow · Keras · scikit-learn · Matplotlib  

---

## 🧠 Results

| Model | Input | Test Acc | Cat F1 | Dog F1 |
|:------|:------|:---------|:-------|:-------|
| Baseline | Full images | 0.76 | 0.60 | 0.82 |
| Cropped + Balanced | Head crops | **0.92** | **0.89** | **0.94** |

Cropping the head regions and balancing classes boosted performance by **+22%**.  
The refined model generalized far better and focused on **morphological cues** like ear shape and snout width instead of background noise.

---

## 💾 Data
**Dataset:** Parkhi et al. (2012). *Oxford-IIIT Pet Dataset*.  
Accessed via [Roboflow](https://universe.roboflow.com/brad-dwyer/oxford-pets)  
**License:** CC BY-SA 4.0

---

## 👤 Author

Moritz Konstantin Kuhn  
Data Science & Communication Research  
📧 [moritzk.kuhn@gmx.com](mailto:moritzk.kuhn@gmx.com)  
🔗 [https://www.linkedin.com/in/moritz-konstantin-kuhn](https://www.linkedin.com/in/moritz-konstantin-kuhn)
