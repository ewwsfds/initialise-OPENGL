# initialise-OPENGL

```
OpenGLApp
│
├── include
│   ├── glad
│   │   └── glad.h
│   └── GLFW
│   │    └── glfw3.h
│   └── KHR
│   │   └── khrplatform.h
│   └── glm
│       └── glm.hpp
│
├── libs
│   ├── glfw
│   │   └── lib-vc2022
│   │     └── glfw3.dll
│   └── glm
│
├── main.cpp
└── sh_image.cpp
└── glad.c


```
Project → Properties → C/C++ → General → Additional Include Directories
```
$(ProjectDir)include
```



Project → Properties → Linker → General → Additional Library Directories
```
$(ProjectDir)libs\glfw\lib-vc2022
```

Linker → Input → Additional Dependencies
```
glfw3.lib
```
