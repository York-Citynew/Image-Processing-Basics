# Image Processing Basics

An **interactive playground for image processing** using **Python, OpenCV, and NumPy**.  
Load an image or use your camera feed, then tweak filters, add noise, run template matching, thresholding, edge detection, and Hough transform fitting — all via **keyboard shortcuts**.

---

## Features

* **Histogram Operations** – live histogram + histogram equalization
* **Brightness & Contrast** – real-time adjustment
* **Noise** – Gaussian; Salt & Pepper
* **Filtering** – Gaussian, Median, Average, Bilateral, Sharpen
* **Windowing** – with preset confidence (default `0.8`)
* **Template Matching** – uses different templates for camera/image modes
* **Thresholding** – cycle through presets
* **Edge Detection** – multiple methods with tunable parameters
* **Boundary Extraction**
* **Hough Transform Fitting** – adjustable resolution and thresholds

---

## Controls

### General

| Key(s)      | Action                                   |
| ----------- | ---------------------------------------- |
| **h**       | Toggle histogram                         |
| **H**       | Cycle Hough transform mode               |
| **w**       | Toggle windowing                         |
| **W**       | Toggle histogram equalization            |
| **t**       | Toggle template matching                 |
| **c**       | Toggle camera (resets cursor to `(0,0)`) |
| **o**       | Toggle boundary extraction               |
| **q**       | Quit program                             |
| **Right Click** | Save the current image/frame to the directory of the notebook |

### Adjustments

| Key(s)    | Action                                  | Range       |
| --------- | --------------------------------------- | ----------- |
| **X / x** | Increase / decrease contrast            | −10 … +10   |
| **B / b** | Increase / decrease brightness          | −255 … +255 |
| **G / g** | Increase / decrease Gaussian noise      | 0 … 10      |
| **P / p** | Increase / decrease Salt & Pepper noise | 0 … 10      |

### Filters

| Key(s)    | Filter    | Kernel Size |
| --------- | --------- | ----------- |
| **Z / z** | Gaussian  | odd, ≥ 1    |
| **M / m** | Median    | odd, ≥ 1    |
| **A / a** | Average   | odd, ≥ 1    |
| **L / l** | Bilateral | odd, ≥ 1    |
| **S / s** | Sharpen   | odd, ≥ 1    |

#### Bilateral parameters

| Key(s)     | Parameter        | Range  |
| ---------- | ---------------- | ------ |
| **+ / =**  | sigmaColor + / − | 0 … 10 |
| **- / \_** | sigmaSpace − / + | 0 … 10 |

---

## Thresholding

Cycle through the following presets:

**Available methods:** `off`, `mean`, `median`, `otsu`, `adaptive`

| Key(s) | Action                                                    |
| ------ | --------------------------------------------------------- |
| **\|** | Cycle thresholding preset (Shift + `\` on most keyboards) |

The current selection is shown on-screen (e.g., `threshold=mean`).

---

## Edge Detection

| Key(s)    | Action                                       | Notes                  |
| --------- | -------------------------------------------- | ---------------------- |
| **e**     | Cycle edge detection method                  | Sobel, Canny, Laplacian|
| **} / ]** | Increase / decrease edge kernel size         | 7 ≥ k ≥ 3              |
| **0 / )** | Decrease / increase **Canny** high threshold | ≥ 0                    |
| **9 / (** | Decrease / increase **Canny** low threshold  | ≥ 0                    |
| **' / "** | Decrease / increase **Laplacian** threshold  | step = 0.05            |

> Tip: A light blur before edge detection often improves results.

---

## Hough Transform

| Key(s)    | Action                                        | Notes                |
| --------- | --------------------------------------------- | -------------------- |
| **H**     | Cycle Hough transform mode                    | Line, Circle         |
| **r / R** | Decrease / increase rho (distance) resolution | min 1                |
| **; / :** | Decrease / increase degree resolution         | min 1                |
| **/ / ?** | Decrease / increase Hough threshold (votes)   | min 1                |
