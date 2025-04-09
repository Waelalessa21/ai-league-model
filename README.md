# 🧠 AI League – Crowd Counting with CSRNet

Welcome to the **AI League Crowd Counting Model** – a deep learning solution powered by **CSRNet** that estimates the number of people in crowded scenes using computer vision. This model helps monitor crowd density and flow with high accuracy, making it ideal for stadiums, especially during major events like the World Cup, as it enhances the overall fan experience.

---

## 📌 Overview

CSRNet (Congested Scene Recognition Network) is a convolutional neural network designed for **crowd counting**. It outputs both a **density map** and an **estimated count** of individuals in the image.

- 🔍 **Detects**: Number of people in crowd scenes.
- 🧭 **Outputs**: Density map + total count.
- 🚀 **Technology**: PyTorch + VGG16 frontend with dilated convolutions.

---

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Waelalessa21/ai-league-model.git
cd ai-league-model
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

Or manually install the core dependencies:

```bash
pip install torch torchvision pillow numpy
```

---

## 📸 Usage Example

### Inference Script

```python
from PIL import Image
from model import CSRNet, predict_density

image = Image.open("crowd.jpg")
count, density_map = predict_density(image)

print(f"Estimated Crowd Count: {count}")
```

> ✅ Make sure you have the pretrained weights: `csrnet_weights.pth`

### Output
- 🔢 **Count**: Integer number of people.
- 🗺️ **Density Map**: A NumPy heatmap showing crowd distribution.

---

## 🧪 Model Loading

```python
model = CSRNet().to(device)
model.load_state_dict(torch.load("csrnet_weights.pth", map_location=device))
model.eval()
```

---

## 📈 Future Enhancements

- Add support for video input and real-time detection.
- Improved visualization for density heatmaps.

---

## 👥 Authors

* Abdullah Al-Mudayris – UX / UI Designer

* Khalid Al-Yami – Developer

* Abdulrahman Al-Busaad – Product Manager

* Wael Al-Essa – Developer

* Azzam Al-Kulaib – Developer

---

## 📝 License

This project was developed as part of a hackathon competition and is not currently open-source.

