# 🎨 Neural Style Transfer using PyTorch

This project implements **Neural Style Transfer** using a pre-trained VGG19 model to generate artistic images by combining the content of one image with the style of another.

---

## 🚀 Project Overview

Neural Style Transfer is a deep learning technique that blends:

- 🖼️ **Content Image** → Structure of the image  
- 🎨 **Style Image** → Artistic appearance  

The output is a new image that preserves the content while adopting the style.

---

## 🧠 How It Works

1. Load content and style images  
2. Resize and convert them into tensors  
3. Use a pre-trained VGG19 model to extract features  
4. Compute:
   - Content Loss → preserves structure  
   - Style Loss → applies artistic texture  
5. Optimize a target image to minimize both losses  

---

## 🛠️ Technologies Used

- Python  
- PyTorch  
- Torchvision  
- PIL (Python Imaging Library)  
- Matplotlib  
- Google Colab  

---

## ⚙️ Implementation Details

### 🔹 Image Processing
- Images resized to **256 × 256**
- Converted to tensors for model input  

### 🔹 Model
- Pre-trained **VGG19**
- Used only feature extraction layers  

### 🔹 Optimization
- Optimizer: Adam  
- Iterations: 30  
- Learning Rate: 0.01  

---

## 📊 Output

The model generates a **styled image** that combines:

- Content from the original image  
- Style from the artistic image  

---

## ⚠️ Challenges Faced

- Runtime errors due to computation graph reuse  
- Memory limitations in CPU environment  
- Handling image loading errors  

### ✅ Solutions

- Used `.detach()` to fix backward errors  
- Froze VGG19 model parameters  
- Reduced image size and iterations  
- Used stable image loading with `BytesIO`  

---

## 💡 Key Learnings

- Understanding feature extraction using CNNs  
- Difference between content and style representations  
- Working with PyTorch autograd and optimization  
- Debugging real-world deep learning issues  

---

## 🔮 Future Improvements

- Increase image resolution for better quality  
- Use GPU for faster processing  
- Build a web app for user interaction  

---

## 👩‍💻 Author

Leena  

---

## ⭐ Conclusion

This project demonstrates how deep learning models can creatively transform images by combining structure and artistic style, showcasing the power of neural networks in computer vision.
