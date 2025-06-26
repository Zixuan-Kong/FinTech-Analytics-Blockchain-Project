# **FinTech Coursework Assignment**

## **1. Explore the Bitcoin Blockchain and Basic Web Coding (10 marks)**

### **1.1 Extract Information From Your Own Transaction (5 marks)**

**Task Instructions**:

* Go to your **Handcash Wallet** transaction history.
* Locate one **micropayment transaction** (e.g., from the initial survey).
* Use the **wallet’s “View on Blockchain”** feature to identify the **block height** of the transaction.

**In Jupyter Notebook**:

* Use the **Whatsonchain API**:

  ```
  https://api.whatsonchain.com/v1/bsv/main/block/height/{blockHeight}
  ```
* Extract and print the following data in **JSON format**:

  * `txcount` – Number of transactions in the block
  * `time` – Unix timestamp (convert it to human-readable time)
  * `totalFees` – Total transaction fees in the block
  * `confirmations` – Number of confirmations the block has
  * `miner` – The mining pool or individual who mined the block

**Additional Requirement**:

* Include Python code that converts the **UNIX timestamp** into a human-readable datetime format (to the nearest second).
* Explain the meaning of each extracted field in plain language.

---

### **1.2 Basic Web Coding (5 marks)**

**Use Reference**: [Satolearn.com Wallet Workshop Materials](https://satolearn.com)

**Task**: Create a simple local web wallet using **HTML + JavaScript + CSS**, which includes the following:

1. **Generate a random private key** (do not show it on the page).
2. Generate a **public key and address** from the private key.
3. Create a **QR code** for the address (to receive payments).
4. Include **custom styling with CSS** (your personal touch).
5. Display **live cryptocurrency price** on your webpage using any API (e.g., CoinGecko, CoinDesk).

> Note: The wallet does **not need to be hosted or store any keys**. It can refresh and generate a new address on every open.

---

## **2. Time Series Investigation of Bitcoin Price (45 marks)**

### **2.1 Obtain Time Series Data (5 marks)**

**Requirement**:
Use **FRED API** or other APIs (Yahoo Finance, Quandl, etc.) to obtain and **plot** 3 time series in a Jupyter Notebook:

1. A **cryptocurrency or high-risk asset** (e.g., Bitcoin).
2. A **safe asset** (e.g., gold price or blue-chip stock).
3. A **market index** (e.g., S\&P 500).

> Make sure all plots are clearly labeled.

---

### **2.2 Data Transformations (10 marks)**

**Steps**:

1. Use the **longest available time span** for each series.
2. Combine the 3 series into one **Pandas DataFrame** with synchronized time periods.
3. Calculate **log returns**:

   $$
   \text{Return}_t = \ln\left(\frac{x_t}{x_{t-1}}\right)
   $$

---

### **2.3 Data Analysis (30 marks)**

**Tasks**:

* Compute the **correlation** between:

  * Risky asset returns vs. safe asset returns
  * Risky asset returns vs. market returns
* Interpret in terms of **CAPM theory**.

**CAPM Regression**:

$$
r_{bt} - r_{ft} = \alpha_b + \beta_b(r_{mt} - r_{ft}) + u_{bt}
$$

* Use **OLS regression** to estimate:

  * $\alpha_b$: Intercept (should be 0 under CAPM)
  * $\beta_b$: Systematic risk (slope)
* Provide interpretation and discussion of results.

---

## **3. Machine Learning in Practice (45 marks)**

### **3.1 Description of FinTech Firm (25 marks)**

**Task**: Based on Sarunas’ project (see Moodle or GitHub repo):

* Write a **non-technical description** of the firm.
* Explain how the **four structural parts** of the firm interact and function.
* Provide a basic description of:

  * **Logistic Regression**: What it does, how it works.
  * How it compares to:

    * **OLS regression**
    * **GenAI tools (e.g., classification/prediction tasks)**

---

### **3.2 Written Description of Python Code (5 marks)**

**Steps**:

* Download Sarunas’ dataset from **Kaggle**.
* Reproduce the model in your own **Jupyter notebook** (`model building.ipynb`).
* Select **10 lines of code** and use **Markdown** cells to explain what each line does.
* Do **not** submit the dataset — only your notebook with **code and results**.

---

### **3.3 Build Your Own Machine Learning Model (15 marks)**

**Your choice**:

* Pick any **financial dataset** (e.g., from Kaggle, Yahoo Finance, etc.).
* Choose and implement a **machine learning model** from `scikit-learn`:

  * Examples: Logistic Regression, Random Forest, SVM, etc.
* Use it to **predict financial outcomes**:

  * E.g., asset movement, classification of credit risk, price prediction
* Include:

  * Data loading and preprocessing
  * Model training and evaluation
  * Performance metrics (accuracy, ROC AUC, etc.)


