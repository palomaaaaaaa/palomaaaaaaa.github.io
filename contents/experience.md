## 项目作品 | Projects

---

### 🏗️ 混凝土28天强度预测 | Concrete Compressive Strength Prediction

**背景与问题**  
混凝土配合比设计是土木工程的核心工作之一。传统方法依赖经验公式和大量试配实验，周期长、成本高。本项目利用机器学习模型，基于配合比参数精准预测混凝土28天抗压强度。

**技术方案**
- **数据集**: UCI Machine Learning Repository — Concrete Compressive Strength Dataset（1030条样本，8个特征）
- **特征**: 水泥、高炉矿渣、粉煤灰、水、减水剂、粗骨料、细骨料、龄期
- **模型**: Linear Regression, Random Forest, XGBoost, LightGBM
- **工具**: Python, Scikit-learn, Pandas, Matplotlib, Seaborn

**关键成果**
- XGBoost 模型达到 **R² = 0.92**，RMSE = 4.8 MPa
- 通过 SHAP 分析揭示了水泥用量和龄期是最关键的影响因素
- 对比了4种模型的性能，验证了集成方法在材料性能预测中的优势

**代码仓库**: [github.com/palomaaaaaaa/concrete-strength-prediction](https://github.com/palomaaaaaaa/concrete-strength-prediction)

---

### 🔍 混凝土裂缝图像检测 | Concrete Crack Detection with CNN

**背景与问题**  
基础设施老化是全球性挑战。定期检测混凝土结构表面裂缝对于预防结构失效至关重要。传统人工巡检效率低、主观性强。本项目从零搭建卷积神经网络（CNN），实现裂缝图像的自动识别。

**技术方案**
- **数据集**: 公开混凝土裂缝图像数据集（40,000张，227×227像素，二分类）
- **模型**: 自建 CNN（3层卷积 + 2层全连接），参考 VGG16 架构设计
- **训练策略**: 数据增强（旋转、翻转、亮度调整）、Dropout 正则化、Adam 优化器
- **工具**: Python, PyTorch, OpenCV, Matplotlib

**关键成果**
- 测试集准确率 **96.8%**，F1-Score = 0.967
- 通过 Grad-CAM 可视化模型关注区域，验证模型聚焦于裂缝特征
- 对比了自定义 CNN 与 ResNet-18 迁移学习的性能差异

**代码仓库**: [github.com/palomaaaaaaa/crack-detection-cnn](https://github.com/palomaaaaaaa/crack-detection-cnn)

---

### 💬 工程规范智能问答系统（进行中）| Construction Code RAG Q&A (In Progress)

**背景与问题**  
土木工程师在日常工作中需要频繁查阅大量设计规范和标准（如GB 50010《混凝土结构设计规范》）。传统关键词搜索效率低、难以理解自然语言问题。本项目基于RAG（检索增强生成）架构，构建一个工程规范智能问答系统。

**技术方案**
- **文档处理**: LangChain + PyPDF2 解析规范PDF文档，文本分块
- **向量存储**: OpenAI Embeddings + ChromaDB 向量数据库
- **检索与生成**: 基于语义相似度检索相关条文，GPT-4o 生成回答
- **前端**: Streamlit 构建交互式问答界面

**预期目标**
- 实现"混凝土梁最小配筋率是多少？"这类自然语言问题的精准回答
- 每条回答附带规范条文出处，确保可追溯性

**代码仓库**: Coming Soon
