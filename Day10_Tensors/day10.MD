# 📘 Detailed Guide to Tensors (0D–5D)
**Based on:** *“What are Tensors | Tensor In-Depth Explanation”* video and standard tensor concepts.

---

## 🧠 What is a Tensor?

A **tensor** is simply a **multi-dimensional array of numbers**. In machine learning and deep learning, **data is stored as tensors** — whether it’s a single number, a list of values, or a batch of images or videos.
Tensors generalize:
- Scalars (single values),
- Vectors (1D),
- Matrices (2D),
- And higher dimensions beyond that.

In deep learning libraries like **TensorFlow** or **PyTorch**, tensors store inputs, outputs, intermediate activations, weights, etc.

---

## ⚙️ Core Tensor Terminology

| Property | Meaning |
|----------|---------|
| **Rank** | Number of dimensions (axes) in the tensor. |
| **Shape** | A list of integers giving the size along each axis. |
| **Size** | Total number of elements, computed by multiplying all shape values. |

---

## 🧮 0D Tensor — Scalar

**Definition:**  
A **0-dimensional tensor** contains **only one number** — no shape aside from `()`.

**Shape:** `()`  
**Example:** A temperature reading, a model’s loss, or a probability like `0.85`.  
👉 It’s just a number — *nothing more*.

---

## 📄 1D Tensor — Vector

**Definition:**  
A 1D tensor is a **list of values**, like a single row of numbers.

**Shape:** `(n,)` where `n` is the number of elements.

**Real-world examples:**
- A feature vector for a machine learning model like `[age, height, weight]`.
- Word embeddings where each word is a list of numbers describing its meaning.

---

## 🧱 2D Tensor — Matrix

**Definition:**  
A 2D tensor is a **matrix** — think rows and columns.

**Shape:** `(rows, columns)`

**Real-world examples:**
- **Spreadsheet data** where each row is a sample and each column is a feature.
- **Grayscale images** (height × width) — each entry stores brightness.

---

## 🧠 3D Tensor — Height × Width × Channels / Depth

**Definition:**  
Add one more axis — now you have a 3D tensor.

**Shape example:** `(height, width, channels)`

**Real-world examples:**
- **Color images**:
  - Height * width * channels
  - E.g., an RGB image is `(480, 720, 3)` repsenting height, width, and three color channels.

---

## 📦 4D Tensor — Batch of 3D Data

**Definition:**  
When you process many samples at once — like a batch of images — you add another axis.

**Shape:**  
`(batch_size, height, width, channels)`

**Real-world examples:**
- **Batch of images** for training:
  - E.g., 32 RGB images of size `(32, 480, 720, 3)`
- **Sequence of images** (frames of a video without batching). 

---

## 🎞 5D Tensor — Sequence of Frames × Batch

**Definition:**  
A 5D tensor is used for **complex data like videos** or **volumetric scans**.

**Shape:**  
`(batch_size, frames, height, width, channels)`

**Real-world example:**  
Video data:
- You have multiple videos (batch),
- Each video has many frames (time dimension),
- Each frame is a colored image with height and width,
- And channels for colors (e.g., RGB).

So a video tensor might look like:

- (4, (1800, 480, 720, 3))

Where:
- `4` → number of videos,
- `1800` → number of frames per video,
- `480` → height,
- `720` → width,
- `3` → color channels (RGB).

This is exactly the kind of example shown in the video you referenced.

---

## 🔍 Simple Analogies

| Tensor | Everyday Example |
|--------|------------------|
| 0D | A single number on a scoreboard |
| 1D | A weather forecast list `[sunny, rainy]` |
| 2D | Grades table in school |
| 3D | A stack of colored photos |
| 4D | A batch of photo collections |
| 5D | Several video files grouped together |

---

## 🛠 Visual Thinking

- A **scalar** is just a value.
- A **vector** is a list.
- A **matrix** is a table.
- A **3D tensor** is a cube of numbers.
- A **4D tensor** is a list of cubes.
- A **5D tensor** is a list of lists of cubes.

---

## 📌 Summary

Tensors are just **multi-dimensional arrays** — the standard way deep learning frameworks store data. You go from **one number (0D)** up to **rich data like video (5D)** by stacking dimensions.

---

