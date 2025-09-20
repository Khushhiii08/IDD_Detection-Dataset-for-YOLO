# Cleaned IDD Detection Dataset for YOLO

This repository provides a cleaned and preprocessed version of the **IDD Detection Dataset** suitable for training YOLO-style object detection models.

---

## 📌 What is the IDD Detection Dataset?

The **India Driving Dataset (IDD)** is a large-scale dataset focused on **unstructured driving environments**, captured from a front-facing camera mounted on a car driving around **Hyderabad, Bangalore, and their outskirts**.  
👉 [Dataset Details](https://idd.insaan.iiit.ac.in/dataset/details/)

**Key stats (Detection subset):**
- **Total Images:** 46,588  
- **Splits:**
  - Train: 31,569 images  
  - Validation: 10,225 images  
  - Test: 4,794 images  
- **Resolution:** Mostly 1080p, some 720p, and others  
- **Classes:** Vehicles, pedestrians, autorickshaws, animals, traffic lights/signs, etc.  
- **Environment:** Real-world, unstructured Indian road conditions  

---

## 🎯 Purpose of This Repo

This repo provides a **cleaned version** of the IDD Detection dataset, specifically formatted for YOLO training:

- ✅ Extracted all images and XML files into centralized `images/` and `labels/` folders  
- ✅ Converted XML annotations to YOLO format (`class x_center y_center width height`)  
- ✅ Organized YOLO-compatible folder structure (`train/`, `val/`, `test/`) based on split txt files  
- ✅ Removed corrupted images and invalid/missing annotations  
- ✅ Filtered out images with empty label files  
- ✅ Checked and removed negative class IDs  
- ✅ Extracted and standardized class list  
- ✅ Verified bounding boxes for validity  
- ✅ Ensured consistency for smooth YOLO training  

---

## 📂 Repository Structure

```plaintext
-/cleaned_idd_detection/
 ├── images/
 │   ├── train/
 │   ├── val/
 │   └── test/
 ├── labels/
 │   ├── train/
 │   ├── val/
 │   └── test/
 ├── data.yaml          # YOLO dataset config (paths, classes, nc)
└── README.md          # this file
