## 项目作品 | Projects

---

### 🏗️ 混凝土28天强度预测 | Concrete Compressive Strength Prediction

*Predicting 28-day compressive strength of concrete from mix proportions using ensemble machine learning.*

**Background & Problem**  
Concrete mix design is a core task in civil engineering, traditionally relying on empirical formulas and costly trial batches. This project uses machine learning to predict concrete compressive strength directly from mix parameters, accelerating early-stage mix optimization.

**Approach**
- **Dataset**: UCI Machine Learning Repository — Concrete Compressive Strength (1,030 samples, 8 features)
- **Features**: cement, blast-furnace slag, fly ash, water, superplasticizer, coarse & fine aggregate, age
- **Feature engineering**: added water-cement ratio, total binder, and aggregate ratio as physically meaningful features
- **Models**: Linear Regression, Random Forest, Gradient Boosting, XGBoost
- **Interpretability**: SHAP analysis to explain feature contributions

**Key Results**
- Ensemble methods clearly outperform linear regression, confirming strong nonlinear interactions
- SHAP analysis identifies cement content and age as the dominant predictors — consistent with civil engineering theory
- Tools: Python, Scikit-learn, XGBoost, Pandas, Matplotlib, Seaborn

![Model performance comparison — R² and RMSE across four models](static/assets/img/projects/model_comparison.png)

![SHAP summary — feature contributions to prediction](static/assets/img/projects/shap_summary.png)

**Repository**: [github.com/palomaaaaaaa/concrete-strength-prediction](https://github.com/palomaaaaaaa/concrete-strength-prediction)

---

### 🔍 混凝土裂缝图像检测 | Concrete Crack Detection with CNN

*Building a convolutional neural network from scratch to classify concrete surface cracks.*

**Background & Problem**  
Aging infrastructure is a global challenge. Regular inspection of concrete surfaces for cracks is critical to preventing structural failure, yet manual inspection is slow and subjective. This project automates crack detection with deep learning.

**Approach**
- **Dataset**: public concrete crack image dataset (40,000 images, 227×227 px, binary classification)
- **Model**: custom CNN (4 conv blocks + BatchNorm + Dropout + adaptive pooling, ~3.5M parameters)
- **Training**: data augmentation (flip, rotation, color jitter), Adam optimizer, ReduceLROnPlateau, early stopping
- **Interpretability**: Grad-CAM to visualize where the model focuses

**Key Results**
- Achieved effective crack classification with the custom architecture
- Grad-CAM heatmaps confirm the model focuses on crack regions
- On the full 40K-image dataset, this architecture is expected to reach ~96–98% accuracy (literature reference)
- Tools: Python, PyTorch, OpenCV, Matplotlib

![Grad-CAM — visualizing where the CNN focuses](static/assets/img/projects/gradcam.png)

![Confusion matrix](static/assets/img/projects/confusion_matrix.png)

**Repository**: [github.com/palomaaaaaaa/crack-detection-cnn](https://github.com/palomaaaaaaa/crack-detection-cnn)

---

### 💬 工程规范智能问答系统（进行中）| Construction Code RAG Q&A (In Progress)

*Building a retrieval-augmented generation system for querying civil engineering design codes.*

**Background & Problem**  
Civil engineers constantly consult design codes and standards (e.g., GB 50010). Keyword search is inefficient and cannot understand natural-language questions. This project builds a RAG-based Q&A system over engineering code documents.

**Approach**
- **Document processing**: LangChain + PDF parsing with text chunking
- **Vector storage**: OpenAI embeddings + ChromaDB
- **Retrieval & generation**: semantic similarity retrieval with GPT-based answer generation
- **Interface**: Streamlit

**Goal**
- Answer natural-language questions like "What is the minimum reinforcement ratio for concrete beams?"
- Every answer cites the specific code clause for traceability

**Repository**: Coming Soon
