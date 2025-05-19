# Automatic-Cricket-Team-Selection
I participated in the American Express Campus Challenge 2024 and ended up in the Top 3 out of 1300 participants! Over three intense rounds, I developed a cricket team selection model using over 80,000 entries from various datasets. I utilized Python and Pandas to create a model that balanced recent performance with consistency, ultimately helping to assemble the best team on paper. Here's a quick rundown of what I did.
## 📊 Data Processing Steps  

### **Data Cleaning**  
- **Duplicate Removal**: Eliminated duplicate records from the dataset.  
- **Handling Null Values**:  
  - Calculated missing **strike rates** as `total runs / balls faced`.  
  - Estimated missing **runs** using the formula: `economy rate * balls bowled / 6`.  
  - Filled missing **city values** in match-level data using the **venue** column.  
  - Replaced missing values in **categorical columns** with `'unknown'`.  

### **Outlier Detection**  
- Identified **min/max values** for each column.  
- Used the **Interquartile Range (IQR) method** to detect and handle outliers.  

### **Data Type Conversion**  
- Converted **string values** in numerical columns to **integers** for consistency.  

---

## 📈 Statistical Analysis  
Statistical measures were applied to evaluate player performance across multiple dimensions:  

- **Exponential Weighted Moving Average (EWMA)**:  
  - Assigned **higher weights** to more **recent matches**.  
  - Weights decrease **exponentially** over time.  
- **Rolling Window Method**:  
  - Processed match data **sequentially** from most recent to oldest within each **batsman group**.  
- **Consistency Measurement**:  
  - Used **rolling standard deviation** to assess **player consistency**.  

---

## 🎯 Query Execution & Team Selection  
- **Data Filtering & Manipulation**: Used **Pandas** queries to extract relevant insights.  
- **Player Selection**: Identified **top-performing** batsmen and bowlers based on **recent form, consistency, and statistical metrics**.  
- **Balanced Team Formation**: Selected an **optimal mix** of players for a well-rounded team.  

---
