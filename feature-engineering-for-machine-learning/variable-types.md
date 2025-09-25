# Variables

## 🔹 What is a Variable?
- A **variable** is a characteristic, number, or quantity that can be measured or counted.  
- Values of variables can **vary** within a population.  
- **Examples**:  
  - Age → 21, 35, 62  
  - Gender → Male, Female  
  - Income, House Price (e.g., in GBP)  
  - Country of Birth, Eye Colour, Vehicle Make  

---

## 🔹 Main Categories of Variables

### 1. Numerical Variables
- Represent numbers/quantities.  
- **Subtypes**:  
  - **Discrete** → Countable values (e.g., number of children).  
  - **Continuous** → Measurable values (e.g., height, weight).  

### 2. Categorical Variables
- Represent labels or categories.  
- **Subtypes**:  
  - **Nominal** → No order (e.g., eye colour, car brand).  
  - **Ordinal** → Ordered categories (e.g., satisfaction level: low, medium, high).  
  - **Date/Time** → Special category (e.g., transaction date).  

### 3. Mixed Variables
- Contain both strings and numbers (e.g., `Product123`).  

---

## 🔹 Why Variables Matter
- Form the **foundation of datasets**.  
- Type of variable determines **analysis and visualisation methods**.  

---
# Numerical Variables

## 🔹 Definition
- **Numerical variables**: Variables whose values are numbers.  
- Can be further classified into:
  1. **Discrete variables**
  2. **Continuous variables**
  3. **Binary variables** (special case of discrete)

---

## 🔹 Discrete Variables
- Represent **whole numbers / counts** (cannot take fractional values).  
- **Examples**:
  - Number of items bought in a supermarket → 1, 25, 50 (not 3.7).  
  - Number of bank accounts → 1, 2, 3 (not 1.5).  
  - Number of pets or children in a family → 0, 1, 2, 3 (not 2.5).  
- **Key property**: Values do **not cover an entire range**.

---

## 🔹 Continuous Variables
- Represent **any value within a range** (can take fractional/decimal values).  
- **Examples**:
  - Amount paid by a customer → $32.5, $12, $5.20.  
  - House price → Can take any value within the market range.  
  - Time spent on a website → 3.4 sec, 5.1 sec.  
  - Total debt as % of income → 0.2, 0.001, 0.  
- **Key property**: Values can **cover the full range** in a histogram/plot.  

---

## 🔹 Binary Variables (special type of discrete)
- **Definition**: Discrete variables that can take only **two possible values**.  
- **Example**:
  - **Default variable** → Indicates if a customer has defaulted on a loan:  
    - `1` → Defaulted  
    - `0` → Not defaulted  

---

## 🔹 Examples from Financial Dataset
- **Interest rate** → Continuous (can take any value in a range).  
- **Number of credit accounts opened in the last 12 months** → Discrete.  
- **Default (target variable)** → Binary.  

---

## 🔹 Key Takeaways
- **Discrete** → Whole numbers (counts).  
- **Continuous** → Any value within a range (fractions allowed).  
- **Binary** → Special discrete variable with only 2 possible values.  
- Always review **Jupyter Notebook examples** for visualisation and coding practice.

---
# Categorical Variables

## 🔹 Definition
- **Categorical variables**: Variables whose values are selected from a **set of categories/labels**.  
- **Examples**:  
  - Gender → Male, Female  
  - Marital status → Never married, Married, Divorced, Widowed  
  - Loan purpose → Debt consolidation, Car purchase, Wedding expenses  
  - Mobile network provider → Vodafone, Orange  
  - Postcode  

---

## 🔹 Types of Categorical Variables

### 1. Ordinal Variables
- Categories can be **meaningfully ordered**.  
- **Examples**:
  - Student grade → A > B > C > Fail  
  - Days of the week → Monday → Sunday  
  - Education level → Elementary → High school → College → PhD  

### 2. Nominal Variables
- Categories have **no intrinsic order**.  
- All categories are equivalent.  
- **Examples**:
  - Country of birth  
  - Postcode  
  - Vehicle make  
  - Loan purpose  
  - Home ownership (own, rent, mortgage)  

---

## 🔹 Special Considerations
- Categories may sometimes be **encoded as numbers** (e.g., Gender: 0 = Female, 1 = Male).  
  - Still **categorical by nature**, despite numerical encoding.  
- **Identifiers** (e.g., customer ID, account number) are often numeric,  
  but they do **not represent numerical quantities**.  
  - Can be treated as categorical.  

---

## 🔹 Why It Matters
- Correctly identifying categorical variables is crucial for **feature engineering** and  
  deciding whether they should be used in **machine learning models**.  

---

## 🔹 Examples from Loan Dataset
- **Nominal variables** studied in the Notebook:  
  - Home ownership → Own, Rent, Mortgage  
  - Loan purpose → Debt consolidation, Car, Credit card payment, Moving, etc.  
  - Loan status  
- Visualisations show **counts of borrowers** within each category.  

---

## 🔹 Key Takeaways
- **Ordinal** → Ordered categories.  
- **Nominal** → Unordered categories.  
- Numeric encoding doesn’t change a variable’s categorical nature.

---

#  Date/Time (Temporal) Variables

## 🔹 Definition
- **Date-time variables**: Variables that store **dates, times, or both**.  
- **Examples**:  
  - Date of birth → Date only  
  - Date of application → Date in another format  
  - Time of accident → Time only  
  - Payment date → Date + Time  

---

## 🔹 Importance
- Require **special consideration in preprocessing**.  
- Correct handling allows for **data enrichment** by extracting useful features.  
- From date/time variables, we can derive:
  - Day, month, year  
  - Day of week, weekend/weekday  
  - Season  
  - Hour, minute, second  
  - Time differences (e.g., loan duration, repayment delays)  

---

## 🔹 Examples from Loan Dataset
- **Issued date** → Date when money was sent to borrower.  
- **Last repayment date** → Date of borrower’s final repayment.  
- Using these, we can visualise:
  - Number of loans disbursed over time.  
  - Distribution across different **risk categories (A–G)**.  

---

## 🔹 Key Takeaways
- Date/time variables = **temporal data**.  
- Can hold:
  - Date only  
  - Time only  
  - Date + Time  
- Preprocessing is essential to **unlock richer insights**.  


---

# Mixed Variables

## 🔹 Definition
- **Mixed variables**: Variables that contain **both numbers and categories** among their values.  
- Two main types:
  1. Variables with **either numbers OR labels** across observations.  
  2. Variables with **both strings and numbers together** in the same observation.  

---

## 🔹 Type 1: Numbers or Labels (per observation)
- Examples (financial variables):
  - **Number of credit accounts** → Values like `1–100`, or codes for missing data (`Unknown`, `Not verified`, `No match`).  
  - **Number of missed payments** → Values:
    - `1, 2, 3` → Missed payments count  
    - `D` → Defaulted  
    - `A` → Arrangements with lender  

---

## 🔹 Type 2: Strings + Numbers (in same observation)
- Examples:
  - **Cabin** (Titanic dataset) → e.g., `C123`  
  - **Ticket** (Titanic dataset) → mix of numbers and letters  
  - **Vehicle registration** → e.g., `AB12 XYZ`  
  - **Postcode** → e.g., `SW1A 1AA`  

---

## 🔹 Why They Matter
- Mixed variables can be **enriched** by separating their:
  - **String components** (e.g., cabin letter, postcode area)  
  - **Numeric components** (e.g., ticket number, postcode digits)  
- Provide additional features for **analysis and modelling**.  

---

## 🔹 Key Takeaways
- Mixed variables combine numeric and categorical elements.  
- Can appear either as:
  - **Alternative values** (numbers or labels), or  
  - **Combined values** (letters + numbers).  
- Careful **preprocessing and feature extraction** unlocks valuable insights.   




