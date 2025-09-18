
### **1. _Differential Equations and Linear Algebra_ (2018)**

**Focus:**

- **Mathematical foundations** (linear algebra + differential equations).
    
- **Theoretical depth** with applications in engineering, physics, and dynamical systems.
    

**Best for:**

- People interested in **mathematical modeling, dynamical systems, or scientific computing**.
    
- Those who want a **strong theoretical basis** in linear algebra **combined with differential equations** (useful for control theory, optimization, and PDEs in ML).
    

**Relevance to Core ML:**  
✔ **Linear algebra** (SVD, eigenvectors, matrix decompositions) is **essential for ML**.  
✔ Differential equations are **less directly relevant** to ML (unless working on **neural ODEs, reinforcement learning, or physics-informed ML**).

---

### **2. _Linear Algebra and Learning from Data_ (2019)**

**Focus:**

- **Applied linear algebra** (with direct applications to ML and data science).
    
- **Learning from data** (regression, PCA, deep learning, optimization).
    

**Best for:**

- **Core ML researchers & practitioners** who want **linear algebra + ML applications**.
    
- People who prefer **intuitive explanations** (Strang’s style) with **real-world ML examples**.
    

**Relevance to Core ML:**  
✔ **Covers PCA, least squares, SGD, and neural networks**—directly applicable to ML.  
✔ Explains **how linear algebra powers ML algorithms** (e.g., backpropagation, embeddings).  
✔ More **modern and ML-focused** than the 2018 book.

---

### **Which One Should You Choose?**

|**Criteria**|**Differential Eqns & LA (2018)**|**LA & Learning from Data (2019)**|
|---|---|---|
|**Primary Focus**|Math theory + DEs|Applied LA + ML|
|**Best for ML Core?**|❌ (Unless doing NN theory)|✅ (Directly relevant)|
|**Covers Deep Learning?**|❌|✅ (Neural nets, backprop)|
|**Useful for Optimization?**|✅ (ODE/PDE connections)|✅ (SGD, least squares)|
|**Readability**|Dense (math-heavy)|More intuitive, ML examples|

---

### **Final Recommendation**

- **For core ML people**, **"Linear Algebra and Learning from Data" (2019)** is the **clear winner**—it’s **more aligned with modern ML** (PCA, deep learning, optimization).
    
- The **2018 book** is better for **mathematicians/physicists** needing **differential equations** alongside linear algebra.
    

**If you already know linear algebra well**, the 2019 book will help you **connect it to ML**. If you need **pure math foundations first**, the 2018 book is better.

Would you like a **chapter-wise breakdown** of the 2019 book’s ML-relevant content? 🚀

<hr>
<hr>



### **Comparison: Boyd & Vandenberghe’s _Convex Optimization_ vs. _Applied Linear Algebra_**

Both books are **excellent** and written by leading experts, but they serve **different purposes** in machine learning (ML) and optimization. Here’s a breakdown to help you choose:

---

### **1. _Convex Optimization_ (2004, Updated 2018)**

**Focus:**

- **Theory and algorithms for convex optimization** (gradient descent, duality, SOCP, SDP).
    
- **Mathematical rigor** with proofs, but also practical applications.
    

**Best for:**

- **ML researchers** working on **optimization theory** (e.g., SVM, neural net training, reinforcement learning).
    
- **Those who need deep intuition** on gradient methods, Lagrange multipliers, and convexity.
    
- **People implementing custom optimizers** (e.g., for constrained ML problems).
    

**Relevance to Core ML:**  
✔ **Key for understanding optimization in ML** (SGD, ADAM, proximal methods).  
✔ Covers **duality** (important for SVMs, kernel methods).  
✔ Used in **advanced ML courses** (e.g., Stanford’s EE364).

**Limitations:**  
❌ **Assumes strong math background** (real analysis, linear algebra).  
❌ **Not focused on ML directly**—more general optimization theory.

---

### **2. _Introduction to Applied Linear Algebra_ (2018)**

**Focus:**

- **Practical linear algebra** (vectors, matrices, least squares, PCA).
    
- **Applications in data science, ML, and signal processing**.
    

**Best for:**

- **Beginners in ML/data science** who need **intuitive LA explanations**.
    
- **Engineers/applied scientists** who use **least squares, regression, and PCA**.
    
- **People who prefer computation over proofs** (uses Python examples).
    

**Relevance to Core ML:**  
✔ **Least squares = foundation of linear regression, ridge regression, and deep learning initialization**.  
✔ **PCA, SVD, and matrix factorizations** (essential for embeddings, recommender systems).  
✔ **More accessible** than _Convex Optimization_ (fewer proofs, more applications).

**Limitations:**  
❌ **Doesn’t cover deep learning or advanced optimization**.  
❌ **Less theoretical** (won’t help with convergence proofs).

---

### **Which One Should You Choose?**

|**Criteria**|_Convex Optimization_|_Applied Linear Algebra_|
|---|---|---|
|**Math Level**|Advanced (grad-level)|Beginner-friendly|
|**Focus**|Optimization theory|Practical LA + regression|
|**Best for ML Core?**|✅ (Optimization theory)|✅ (Foundations of ML)|
|**Covers Deep Learning?**|Indirectly (SGD, etc.)|❌ (Only basic LA)|
|**Useful for Implementers?**|✅ (Custom optimizers)|✅ (Regression, PCA)|
|**Python Examples?**|❌ (Mostly math)|✅ (NumPy included)|

---

### **Final Recommendation**

- **For ML researchers & optimization theory**: **"Convex Optimization"** is a **must-read**.
    
- **For applied ML engineers & beginners**: **"Applied Linear Algebra"** is **more practical and accessible**.
    

**If you can, read both** (in order):

1. Start with _Applied Linear Algebra_ to build intuition.
    
2. Move to _Convex Optimization_ for deeper theory.