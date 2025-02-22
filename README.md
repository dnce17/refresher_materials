# useful_references

## Data Cleaning
### Q&A
#### 1. If a row has missing values, should we remove it or put in a filler value like 0?
- Do NOT delete rows with missing values. If a column has a high percentage of missing values (e.g., 95% missing BMI), consider deleting the column instead.
- Experiment by checking accuracy with and without the column before deciding.
- When filling missing values (e.g., median, average, or 0), no single method is universally better—test different approaches to see which yields the best results.
#### 2. In real-world data, how do you handle missing values that aren't detected by pandas (aka aren't NaN) such as '?' and 'Unknown'? Would you use .unique() on all columns and then look at all the values to identify them?
- Certainly wouldn’t hurt to
#### 3. When working with lots of columns, how do you decide which columns to use?
- You don’t need to use all columns—feature selection techniques (e.g., TCA) can reduce 1,000 columns to 50–20.  
- 100 columns is considered manageable in reviewing them all manually 
- At minimum, skim through all columns to understand the dataset better (The more you understand the data, the better)
- Even if not all data is used, it’s crucial to examine everything
- Data cleaning typically takes up **80%** of a data analyst’s time.

### Notes
#### Dropping columns
- In a job, you almost always drop the id column b/c it’s typically irrelevant and can be considered PHI
  - Drop the ID column **BEFORE** checking for duplicates—otherwise, every row will be unique, preventing duplicate detection.
- In general, you drop irrelevant columns or columns considered PHI (e.g. SSN, apt number, or columns that are irrelevant to what you're trying to find)
  - E.g. You might keep county, city, and state, but remove apt numbers b/c conclusions derived from apartment 1A vs 1B are likely not to be useful

TO FINISH LATER - CHECKPOINT Session 3
