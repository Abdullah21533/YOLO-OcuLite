# Instructions for Using the Demo Notebook

This repository includes the **YOLO-OcuLite demonstration notebook**:  
`Demo_Yolo_Oculite.ipynb`

The notebook is fully integrated into version control by committing it directly to the **main branch** of this repository.  
This ensures that the entire pipeline is versioned, reproducible, and accessible to anyone collaborating or using the project.

---

## 🔄 What the Notebook Demonstrates
The notebook provides a complete, end-to-end workflow of **YOLO-OcuLite**, covering the following steps:

1. **Environment Setup**  
   - Installing required Python libraries  
   - Ensuring GPU availability in Google Colab  

2. **Model Loading**  
   - Automatically loads the pretrained YOLO-OcuLite weights (`YOLO_OcuLite.pt`)  

3. **Dataset Access**  
   - Reads example eye images (BPE, APE, VPE, NE) from the provided dataset  

4. **Inference**  
   - Runs YOLO-OcuLite detection on each image  
   - Produces bounding boxes and subtype classification (Bacterial, Allergic, Viral, Normal)  

5. **Saliency Map Generation (OcuMap)**  
   - Uses an EigenCAM-based method for explainable AI  
   - Generates class-specific heatmaps showing pathology-relevant features  
   - Produces side-by-side triptych outputs (Original Image | OcuMap | Detection Result)  

6. **Results & Outputs**  
   - Saves generated images and triptychs to the `runs/` directory  
   - Allows both visualization inside Colab and export to local storage  

---

## 🚀 How to Run in Google Colab
1. Open the repository in GitHub.  
2. Locate the file: **`Demo_Yolo_Oculite.ipynb`**  
3. Click the **Open in Colab** badge (or open directly in Google Colab).  
4. Once the notebook is open, select **Runtime → Run all**.  

Colab will automatically:  
- Install dependencies  
- Load the YOLO-OcuLite model  
- Run inference on the provided dataset  
- Generate detection results and **OcuMap** visualizations  

---

## 📂 Outputs
After running, you will find:  
- **Detections** → bounding box results for each input image  
- **OcuMap visualizations** → heatmaps showing model attention  
- **Triptych images** → combined visualizations for easier interpretation  

All outputs are saved in the folder:  
