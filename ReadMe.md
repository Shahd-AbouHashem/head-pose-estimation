#  Head Pose Estimation Project

This project focuses on **head pose estimation** using facial landmarks extracted with **MediaPipe**, and prediction using traditional machine learning models like **SVM, KNN, and SGD**. It includes both **regression models (pitch, yaw, roll)** and **orientation classification (Front, Left, Right, Up, Down)**.

---

##  Project Structure

```
 head-pose-project/
│
├── Milestone1_colab.ipynb       <- Head pose regression (training + inference)
├── Milestone2_colab.ipynb       <- Orientation classifier (training + inference)
├── milestone1.ipynb             <- Final cleaned code for Milestone 1 (you can skip training and use directly)
├── milestone2.ipynb             <- Final cleaned code for Milestone 2 (you can skip training and use directly)
├── svm_pitch_model2.pkl         <- Pre-trained SVM model for pitch
├── svm_yaw_model2.pkl           <- Pre-trained SVM model for yaw
├── svm_roll_model2.pkl          <- Pre-trained SVM model for roll
├── head_orientation_classifier.h5 <- Trained Keras model for head orientation classification
├── requirements.txt             <- Required libraries
└── README.md                    <- Project documentation
```

---

## How to Use

###  **Milestone 1 - Regression (Pitch, Yaw, Roll)**

* **Notebook**: `Milestone1_colab.ipynb`
* **Goal**: Predict pitch, yaw, and roll angles from normalized 468 facial landmarks.
* You can **skip training** and directly use the pre-trained models:

  * `svm_pitch_model2.pkl`
  * `svm_yaw_model2.pkl`
  * `svm_roll_model2.pkl`
* Just change the model loading path inside the notebook:


---

###  **Milestone 2 - Orientation Classification**

* **Notebook**: `Milestone2_colab.ipynb`
* **Goal**: Classify head orientation as `Front`, `Left`, `Right`, `Up`, or `Down` using pitch/yaw values.
* You can either:

  * Use the **pre-trained model**: `head_orientation_classifier.h5`
  * Or **re-train** the model using the notebook (edit hyperparameters as needed)

---

##  Dataset

We used the **AFLW2000 dataset**, available at:
👉 [http://www.cbsr.ia.ac.cn/users/xiangyuzhu/projects/3DDFA/main.htm](http://www.cbsr.ia.ac.cn/users/xiangyuzhu/projects/3DDFA/main.htm)

This dataset contains:

* 2000 images
* `.mat` files with ground truth pitch, yaw, roll angles
* Each image annotated with 68 or 468 landmarks

---

## Installation

```bash
pip install -r requirements.txt
```



## Author

Developed by Huda Hesham 


