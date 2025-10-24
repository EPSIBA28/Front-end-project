Json
{
  "images": [
    "images/slide1.jpg",
    "images/slide2.jpg",
    "images/slide3.jpg"
  ]
}
---

### **6️⃣ Final Submission**

**Deliverables:**
- ✅ GitHub Repository Link  
- ✅ Live Deployed Link (GitHub Pages / Netlify)  
- ✅ Project Report (PDF/Doc)  
- ✅ Screenshots  
- ✅ README & Setup Guide  

---

## 💻 **Dynamic Image Slider — Code**

Here’s a complete example:

### **index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dynamic Image Slider</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="slider">
    <div class="slides" id="slides"></div>
    <button class="prev" onclick="prevSlide()">&#10094;</button>
    <button class="next" onclick="nextSlide()">&#10095;</button>
  </div>

  <script src="script.js"></script>
</body>
</html>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #111;
}

.slider {
  position: relative;
  width: 80%;
  max-width: 800px;
  overflow: hidden;
  border-radius: 10px;
}

.slides {
  display: flex;
  transition: transform 0.8s ease-in-out;
}

.slides img {
  width: 100%;
  border-radius: 10px;
}

.prev, .next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(255,255,255,0.5);
  border: none;
  padding: 10px;
  cursor: pointer;
  font-size: 24px;
  border-radius: 50%;
}

.prev { left: 10px; }
.next { right: 10px; }

.prev:hover, .next:hover {
  background: #fff;
}
