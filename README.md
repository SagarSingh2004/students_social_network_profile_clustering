# Student Social Network Profile Clustering

## 📋 Project Overview

This project aims to **segment high school students into distinct groups** based on their social networking profile data using **unsupervised machine learning techniques**. By analyzing student interests, demographics, and online behavior, we identify hidden patterns and clusters that can help understand student segmentation and behavioral trends.

### 🎯 Objective
- Segment students into meaningful clusters using clustering algorithms
- Analyze student behavior based on interests and demographics
- Apply and compare multiple clustering algorithms (K-Means, Hierarchical, DBSCAN)
- Evaluate clustering performance using multiple metrics
- Provide actionable insights for student segmentation

---

## 📊 Dataset

### Dataset Information
- **Source:** Social networking platform (2006-2009)
- **Sample Size:** ~15,000 high school students
- **Total Features:** 41 (37 interest-based + 4 demographic)
- **Data Collection Method:** Web crawling and text mining

### Features

#### Interest-Based Features (37)
| Category | Features |
|----------|----------|
| Sports | basketball, football, soccer, softball, volleyball, swimming, cheerleading, baseball, tennis, sports |
| Appearance | cute, sexy, hot, kissed, hair, dress, blonde |
| Entertainment | dance, band, marching, music, rock |
| Religion | god, church, jesus, bible |
| Shopping | mall, shopping, clothes, hollister, abercrombie |
| Other | die, death, drunk, drugs, sex |

#### Demographic Features (4)
| Feature | Description |
|---------|-------------|
| `gradyear` | Graduation year of the student |
| `gender` | Gender of the student (Male/Female) |
| `age` | Age of the student at time of survey |
| `number_of_friends` | Number of friends/contacts on social network |

---

## 🗂️ Project Structure

```
Student-Social-Network-Clustering/
├── 01_project_overview.ipynb          
├── 02_eda.ipynb                       
├── 03_clustering_models.ipynb         
├── data/
│   └── students_data.csv              
├── requirements.txt
├── .gitignore
├── requirements.txt                   
└── README.md                          
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- Jupyter Notebook

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/SagarSingh2004/students_social_network_profile_clustering.git
cd Student-Social-Network-Clustering
```

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

5. **Open notebooks in order:**
   - `01_project_overview.ipynb` - Start here for project context
   - `02_eda.ipynb` - Explore the data
   - `03_clustering_models.ipynb` - Run clustering analysis

---

## 📦 Dependencies

The project requires the following Python libraries:

```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
scipy>=1.7.0
```

For a complete list, see `requirements.txt`.

---

## 📚 Project Workflow

### Phase 1: Project Overview ✅
- Problem statement definition
- Data overview and characteristics
- Complete data dictionary (41 features)
- Project objectives and goals
- Tools and libraries used

**Notebook:** `01_project_overview.ipynb`

### Phase 2: Exploratory Data Analysis (EDA) ✅
- Data loading and initial inspection
- Data shape and structure analysis
- Column cleaning and data type conversion
- Statistical summaries and descriptive statistics
- Missing values analysis
- Outlier detection using IQR method
- Distribution analysis and skewness
- Correlation analysis
- Data visualization

**Notebook:** `02_eda.ipynb`

**Key Findings:**
- Dataset quality verified
- Data types corrected (age converted to numeric)
- Missing values identified and handled
- Outliers detected and documented
- Feature distributions understood
- Feature relationships analyzed

### Phase 3: Clustering Models ✅
- Feature engineering and selection
- Scaling method comparison (StandardScaler, MinMaxScaler, RobustScaler)
- Dimensionality reduction with PCA (2-30 components)
- Multiple clustering algorithms:
  - **K-Means:** Elbow method + Silhouette analysis
  - **Hierarchical Clustering:** Ward linkage
  - **DBSCAN:** Parameter tuning (eps, min_samples)
- Model evaluation and comparison
- Cluster visualization

**Notebook:** `03_clustering_models.ipynb`

**Best Configuration Found:**
- Algorithm: K-Means
- Scaler: MinMaxScaler
- PCA Components: 2
- Optimal K: Determined by silhouette score
- Validation: Cluster balance verified

---

## 🔍 Methodology

### Data Preprocessing
```
Raw Data → Feature Selection → Scaling → Dimensionality Reduction → Clustering
```

### Scaling Methods Tested
1. **StandardScaler** - Mean normalization with standard deviation
2. **MinMaxScaler** - Scales features to [0, 1] range ✅ BEST
3. **RobustScaler** - Uses median and IQR for robustness

### Dimensionality Reduction
- **PCA (Principal Component Analysis)** tested with 2-30 components
- Best result: **PCA(n_components=2)** for optimal clustering

### Clustering Algorithms

#### K-Means Clustering
- Tests K values from 2 to 10
- Elbow method to identify optimal K
- Silhouette score evaluation
- Cluster balance verification

#### Hierarchical Clustering
- Four linkage method:
  - Ward (minimizes variance)
- Dendrogram visualization
- Silhouette score evaluation

#### DBSCAN
- Density-based clustering
- Parameter tuning (eps, min_samples)
- Noise point identification
- Cluster validation

### Evaluation Metrics
- **Silhouette Score:** Range [-1, 1], measures cluster quality
- **Cluster Balance:** Distribution of samples across clusters
- **Visualizations:** 2D scatter plots and dendrograms
- **Value Counts:** Verification of meaningful cluster distributions

---

## 📈 Results

### Final Model Selection
**Best Clustering Configuration:**
- **Algorithm:** K-Means
- **Preprocessing:** MinMaxScaler + PCA(2)
- **Optimal K:** Determined by silhouette score
- **Validation:** Balanced, meaningful clusters

### Key Outcomes
✅ Identified optimal number of student clusters  
✅ Determined best preprocessing approach  
✅ Compared multiple clustering algorithms  
✅ Evaluated cluster quality with multiple metrics  
✅ Provided actionable student segmentation  

### Business Insights
- Students can be segmented into **distinct interest-based groups**
- **Demographic patterns** correlate with student interests
- Clustering enables identification of:
  - Interest communities
  - Behavioral patterns
  - Peer groups
  - Targeted engagement opportunities

---

## 📊 Visualizations

The project generates multiple visualizations:

### Exploratory Data Analysis
- Distribution plots for each feature
- Correlation heatmaps
- Box plots for outlier detection
- Histograms for skewness analysis

### Clustering Results
- Elbow curve (K-Means)
- Silhouette score comparison
- 2D scatter plots of clusters
- Dendrograms (Hierarchical Clustering)
- Cluster distribution bar charts

---

## 🎓 Key Learning Outcomes

This project demonstrates:

1. **End-to-End ML Pipeline**
   - Problem definition → Data exploration → Model development → Evaluation

2. **Data Quality & EDA**
   - Comprehensive data exploration techniques
   - Missing value handling
   - Outlier detection
   - Statistical analysis

3. **Clustering Techniques**
   - Multiple clustering algorithms
   - Hyperparameter tuning
   - Model comparison and selection
   - Proper evaluation methodology

4. **Feature Engineering**
   - Scaling and normalization
   - Dimensionality reduction (PCA)
   - Feature selection

5. **Model Evaluation**
   - Silhouette score interpretation
   - Cluster validity assessment
   - Comparison across algorithms

---

## 💡 How to Use This Project

### For Learning
1. Start with `01_project_overview.ipynb` for context
2. Follow `02_eda.ipynb` to understand EDA process
3. Study `03_clustering_models.ipynb` for clustering techniques
4. Experiment with different parameters and algorithms

### For Replication
```python
# Basic usage example
from sklearn.preprocessing import MinMaxScaler
from sklearn.decomposition import PCA
from sklearn.cluster import KMeans

# Prepare data
scaler = MinMaxScaler()
X_scaled = scaler.fit_transform(X)

# Apply PCA
pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

# Cluster
kmeans = KMeans(n_clusters=optimal_k, random_state=42, n_init=20)
labels = kmeans.fit_predict(X_pca)
```

### For Extension
- Test additional scaling methods
- Experiment with different PCA components
- Try other clustering algorithms
- Apply ensemble methods
- Add more evaluation metrics

---

## 📝 Notebooks Description

### 01_project_overview.ipynb
**Purpose:** Project setup and data understanding  
**Contents:**
- Problem statement and objectives
- Data overview and characteristics
- Complete data dictionary with 41 features
- Project goals and scope
- Tools and libraries used

**Time to Complete:** 5-10 minutes (reading only)

### 02_eda.ipynb
**Purpose:** Comprehensive data exploration  
**Contents:**
- Data loading and initial inspection
- Data quality checks
- Statistical analysis
- Missing value analysis
- Outlier detection
- Distribution and skewness analysis
- Correlation analysis
- Data visualization

**Time to Complete:** 15-20 minutes

### 03_clustering_models.ipynb
**Purpose:** Clustering algorithm development and evaluation  
**Contents:**
- Feature preparation and selection
- Scaling method comparison
- PCA dimensionality reduction
- K-Means clustering with elbow method
- Hierarchical clustering with dendrograms
- DBSCAN clustering with parameter tuning
- Model evaluation and comparison
- Results visualization

**Time to Complete:** 20-30 minutes (depending on dataset size)

---

## 🔧 Troubleshooting

### Common Issues

**Issue:** Memory error with large dataset
```bash
# Solution: Work with data batches or sample the data
df_sample = df.sample(n=10000, random_state=42)
```

**Issue:** Slow PCA computation
```bash
# Solution: Reduce number of components to test
components = [2, 5, 10, 20]  # Instead of 2-30
```

**Issue:** Inconsistent clustering results
```bash
# Solution: Set random_state for reproducibility
kmeans = KMeans(n_clusters=k, random_state=42, n_init=20)
```

---

## 📚 Resources & References

### Scikit-learn Documentation
- [K-Means Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Hierarchical Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html)
- [DBSCAN](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html)
- [Silhouette Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html)
- [PCA](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)

### Learning Materials
- [Clustering Algorithms Overview](https://en.wikipedia.org/wiki/Cluster_analysis)
- [Silhouette Analysis](https://scikit-learn.org/stable/auto_examples/cluster/plot_silhouette_analysis.html)
- [PCA Explained](https://en.wikipedia.org/wiki/Principal_component_analysis)

---

## 👨‍💼 Author

**Sagar Singh / Aspiring Data Scientist**  
- GitHub: [SagarSingh2004](https://github.com/SagarSingh2004)
- LinkedIn: [LinkedIn](https://linkedin.com/in/sagar-s-10a53028a)
- Email: itsofficialworkforss@gmail.com

---

## 🗓️ Project Timeline

- **Phase 1:** Project Definition & Planning ✅
- **Phase 2:** EDA & Data Understanding ✅
- **Phase 3:** Clustering Model Development & Evaluation ✅
- **Phase 4:** Documentation & README ✅

---
