<h1>Real-Time Label Detection and Information Extraction</h1>

<h2>Description</h2>
This project involves the development of a real-time system for detecting labels on packaging and extracting critical information, such as lot numbers, manufacturing dates, and supplier IDs. The system is designed to enhance traceability by combining label detection and Optical Character Recognition (OCR). It integrates multiple components to achieve reliable real-time performance, making it suitable for industrial deployment.  
<br />

<h2>Technologies Used</h2>
- <b>YOLOv10</b> (for label detection)  
- <b>EasyOCR</b> (for text extraction)  
- <b>OpenCV</b> (for preprocessing and visualization)  
- <b>Roboflow</b> (for annotating images in COCO format)  

<h2>Environments Used</h2>
- <b>Python</b>  
- <b>Google Colab</b> 

<h2>Project Workflow</h2>

<h3>1. Data Collection and Annotation</h3>
<p>
The project starts with collecting images of packaging labels and annotating them using **Roboflow**. Labels are carefully marked to create a high-quality dataset. This dataset is exported in the COCO format, ensuring compatibility with the YOLOv8 training pipeline.
</p>

<p align="center">
  Annotating the images with **Roboflow**: <br/>
  <img src="https://i.imgur.com/QqCt6Rb.png" height="80%" width="80%" alt="Data Annotation Step"/><br />
</p>

<h3>2. Label Detection Model (YOLOv10)</h3>
<p>
The annotated dataset is used to train a YOLOv8 model for detecting labels on packaging. The model achieves high accuracy in detecting labels under diverse conditions. Training and evaluation metrics, such as mean average precision (mAP), are used to ensure the robustness of the model.
</p>

<h3>3. Text Extraction Using OCR</h3>
<p>
Once the labels are detected, the **EasyOCR** module is used to extract text from the detected label regions. This step focuses on identifying lot numbers, manufacturing dates, and supplier IDs, even when the text formats vary.
</p>

<h2>Evaluation</h2>
<p>
To evaluate the performance of the label detection model, I analyzed the **precision-confidence curve**, which measures the model's precision across varying confidence thresholds. The curve provides insights into the model's ability to accurately detect labels at different levels of confidence.
</p>

<p align="center">
  Precision-Confidence Curve: <br/>
  <img src="https://i.imgur.com/bxNplHm.png" height="80%" width="80%" alt="Precision-Confidence Curve"/><br />
</p>

<p>
The curve shows that the model maintains high precision at confidence levels above 0.5, indicating strong reliability in label detection. Additionally, metrics such as mean average precision (mAP) and recall are evaluated to ensure comprehensive assessment.
</p

<h3>4. Real-Time Deployment and Integration</h3>
<p>
The label detection and OCR modules are integrated into a single pipeline for real-time operation. The system runs on a **Raspberry Pi 4** with a camera module to capture images in real time, detect labels, and extract information seamlessly. The final output is displayed and stored for further traceability purposes.
</p>

<h2>Results</h2>
<p>
The integrated system is tested on real-world packaging images. Below is an example of the final result showing detected labels and extracted information in real time:
</p>

<p align="center">
  Final result with label detection and extracted text: <br/>
  <img src="https://i.imgur.com/nL0ZzSR.png" height="80%" width="80%" alt="Final Result"/><br />
</p>
<p align="center">
  <img src="https://i.imgur.com/xPMNW1i.png" height="80%" width="80%" alt="Final Result"/><br />
</p>
