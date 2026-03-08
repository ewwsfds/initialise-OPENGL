# 🧱 Initialise OPENGL (Windows + C++)

A simple guide to setting up **OpenGL** using **GLFW**, **GLAD**, and **GLM** on Windows.

---

## 📦 Step 1 — Download Libraries

### 🪟 GLFW (Window & Input)
Download:
```
https://www.glfw.org/download.html
```
Choose:
> Pre-compiled binaries → Windows 64-bit

---

### ⚙️ GLAD (OpenGL Loader)
Generate at:
```
https://glad.dav1d.de
```

Settings:

• Language → C/C++  
• API → OpenGL  
• Version → Latest  
• Profile → Core  
• Generate Loader → YES  

Click **Generate** and download the zip.

---

### ➗ GLM (Math Library)
Download:
```
https://github.com/g-truc/glm
```

---

## 📁 Project Structure

```
OpenGLApp
│
├── include
│   ├── glad
│   │   └── glad.h
│   ├── GLFW
│   │   └── glfw3.h
│   ├── KHR
│   │   └── khrplatform.h
│   └── glm
│       └── glm.hpp
│
├── libs
│   ├── glfw
│   │   └── lib-vc2022
│   │       └── glfw3.dll
│   └── glm
│
├── main.cpp
├── sh_image.cpp
└── glad.c
```

---

## ⚙️ Visual Studio Configuration

### ➤ Additional Include Directories
`Project → Properties → C/C++ → General`

```
$(ProjectDir)include
```

---

### ➤ Additional Library Directories
`Project → Properties → Linker → General`

```
$(ProjectDir)libs\glfw\lib-vc2022
```

---

### ➤ Linker Dependencies
`Linker → Input → Additional Dependencies`

```
glfw3.lib
```

---

## ▶️ Build & Run

If setup is correct:

✅ Project builds without errors  
✅ A window opens  
✅ OpenGL is ready  

---

## 💡 Notes

• `.lib` files are for linking during build  
• `.dll` files are required at runtime (place next to `.exe`)  
• Make sure **x64** project matches **64-bit GLFW**

---

## 🚀 Next Steps

After setup you can learn:

• Drawing your first triangle  
• VBO / VAO / Shaders  
• Textures  
• Model loading  
• Camera movement  

---

Made for beginners getting started with OpenGL ❤️
