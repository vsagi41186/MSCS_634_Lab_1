# MSCS_634_Lab_1
# Brain Tumor Feature Analysis  
### Vinay Varma Sagi
### Course: MSCS 634 – Data Science and Machine Learning  
### Lab Title: Data Visualization, Preprocessing, and Statistical Analysis  


## 📘 Purpose of the Lab

The primary goal of this lab was to explore, visualize, preprocess, and analyze a dataset titled **“Brain Tumor.csv”**, which contains both first- and second-order statistical features extracted from brain tumor images. The dataset consists of **5,762 samples and 15 columns**, including image identifiers, various quantitative texture and intensity features, and a binary target variable labeled **“Class”**, where `1` represents the presence of a tumor and `0` indicates a non-tumor case. This lab aimed to demonstrate proficiency in applying data science techniques—ranging from visualization and data cleaning to statistical computation and correlation analysis—using Python libraries such as `pandas`, `numpy`, `matplotlib`, and `seaborn`. Each stage of the process provided insights into data structure, relationships among variables, and overall data quality, preparing the dataset for future predictive modeling or diagnostic interpretation.



## 📊 Key Insights from Visualizations and Statistical Measures

The exploratory visualizations provided several meaningful observations about the dataset. The **scatter plot of Mean vs. Variance** revealed that tumor and non-tumor images exhibit distinct clusters, suggesting that statistical variations in pixel intensity can be useful for classification. **Histograms and box plots** demonstrated that certain features, such as Contrast and Skewness, had skewed distributions with noticeable outliers. Through **bar and pie charts**, it was confirmed that the dataset is moderately imbalanced, with slightly more non-tumor samples than tumor cases.

During preprocessing, **no missing values** were detected, confirming that the dataset was clean and well-formatted. However, **1,089 outliers** were identified using the **Interquartile Range (IQR)** technique, and these were removed to improve data integrity. The dataset was reduced from 3,762 to 2,673 entries. Further reduction included removing the non-numeric “Image” column and performing a **50% random sampling** to create a smaller, more manageable subset. Scaling transformations were applied using **Min-Max normalization** and **Z-score standardization**, ensuring that all numerical attributes were comparable in magnitude.

The **descriptive statistics** revealed that Mean and Variance values varied significantly across images, with high standard deviations indicating wide variability in image texture. Measures of central tendency showed the mean intensity (Mean = 9.48) and variance (≈711) were moderate, while dispersion metrics confirmed considerable spread in the data. The **correlation matrix** revealed strong relationships between features such as Mean and Variance (r = 0.78), Energy and ASM (r = 0.96), and Entropy with Homogeneity (r = 0.99), implying that some features are interdependent. Notably, Class showed moderate positive correlations with Variance and Dissimilarity but negative correlations with Energy and Homogeneity, suggesting texture uniformity might inversely relate to tumor presence.



## ⚙️ Challenges and Decisions

One major challenge encountered during the lab was the presence of extreme outliers that heavily skewed the visualizations and statistical outputs. To mitigate this, the IQR method was applied to systematically identify and remove those outliers while preserving the underlying data patterns. Another challenge involved managing features with near-constant values, such as “Coarseness,” which had minimal variation across samples. This required careful interpretation to avoid misleading statistical results. Additionally, ensuring that scaling did not distort data interpretation required the use of both Min-Max and Z-score methods to compare their effects. Finally, balancing interpretability and computational efficiency led to the decision to apply 50% sampling for demonstration purposes, maintaining representative data while reducing processing time.




