# Image Processing Basics
This repository contains a collection of basic image processing techniques implemented in Python using OpenCV and NumPy.
It serves as an interactive playground to explore and experiment with fundamental concepts like filtering, histogram operations, edge detection, and noise manipulation.
## Note:
If you want to dive deeper into image processing theory, explore more advanced algorithms, or see older experiments, please check my archived image processing repositories for additional explanations, implementation details, and references.

---

The program allows real-time adjustments via keyboard shortcuts.
You can load images or use your camera feed, apply various processing techniques, and fine-tune parameters interactively.

### **Core Functionalities**

* **Histogram Display & Equalization**
* **Windowing**
* **Template Matching**
* **Camera Capture**
* **Edge Detection(Blur before use)**
* **Brightness & Contrast Control**
* **Noise Addition (Gaussian & Salt & Pepper)**
* **Filtering (Gaussian, Median, Bilateral, Average, Sharpen)**

---

## Controls

| Key(s) | Action                                            |
| ------ | ------------------------------------------------- |
| **h**  | Toggle histogram                                  |
| **w**  | Toggle windowing                                  |
| **W**  | Toggle histogram equalization                     |
| **t**  | Toggle template matching                          |
| **c**  | Toggle camera & reset cursor to `(0,0)`           |
| **q**  | Quit program                                      |

### **Adjustments**

| Key(s)    | Action                                  | Range       |
| --------- | --------------------------------------- | ----------- |
| **X / x** | Increase / decrease contrast            | −10 … +10   |
| **B / b** | Increase / decrease brightness          | −255 … +255 |
| **G / g** | Increase / decrease Gaussian noise      | 0 … 10      |
| **P / p** | Increase / decrease Salt & Pepper noise | 0 … 10      |

### **Filters**

| Key(s)    | Filter    | Kernel Size Range |
| --------- | --------- | ----------------- |
| **Z / z** | Gaussian  | min 1             |
| **M / m** | Median    | min 1             |
| **L / l** | Bilateral | min 1             |
| **A / a** | Average   | min 1             |
| **S / s** | Sharpen   | min 1             |

### **Bilateral Filter Parameters**

| Key(s)     | Parameter        | Range  |
| ---------- | ---------------- | ------ |
| **+ / =**  | sigmaColor + / − | 0 … 10 |
| **\_ / -** | sigmaSpace + / − | 0 … 10 |

### **Edge Detection**

| Key(s)    | Action                               | Notes                 |                                  |
| --------- | ------------------------------------ | --------------------- | -------------------------------- |
| \*\*      | \*\*                                 | Next threshold preset | Cycles through available options |
| **} / ]** | Increase / decrease edge kernel size | min 3                 |                                  |

---

* More parts will be added...