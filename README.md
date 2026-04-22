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


### ⚙️ stb_image 
Donwload:
```
https://github.com/nothings/stb
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

### Assimp
Download:
```
https://kimkulling.itch.io/the-asset-importer-lib)
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
│   ├── assimp
│   │   └── Importer.hpp
│   └── glm
│       └── glm.hpp
│
├── libs
│   ├── glfw
│   │   └── lib-vc2022
│   │       └── glfw3.dll
│   ├── assimp
│   │   └── libs
│   │   │  └── assimp-vc143-mt.lib
│   └── glm
│
├── main.cpp
├── stb_image.h
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
### Make sure glad.c is in your project

`Right-click your project → Add → Existing Item → select glad.c`

Now it will compile along with your main.cpp


---

### ➤ Assimp Additional Library Directories
`Project → Properties → Linker → General → Additional Library Directories`

```
$(ProjectDir)libs\assimp\lib
```

### ➤ Linker Dependencies
`Linker → Input → Additional Dependencies`

```
assimp-vc143-mt.lib
```

---
### ➤ Make sure assimp-vc143-mt.dll is inside 64x/debug
