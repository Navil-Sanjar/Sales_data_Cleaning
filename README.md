# Sales_data_Cleaning
This is Sales data Cleaning project source-https://www.kaggle.com/datasets/shivavashishtha/dirty-data-sample?resource=download

# 🧼 Sales Data Cleaning Script

This repo cleans and reshapes messy sales data from the `"Dirty 1"` sheet of the Excel file **Ditry Data Sample.xlsx**.

## 📊 Problem

The original data is arranged in a wide, unstructured format:
- Sales values are spread across unnamed columns
- Each segment (Consumer, Corporate, Home Office) is stored in a different block
- Ship modes (First Class, Same Day, etc.) are split into multiple columns

## ✅ Goal

Transform it into a clean, tidy format:

| Segment      | Ship Mode       | Order ID     | Sales  |
|--------------|------------------|--------------|--------|
| Consumer     | First Class      | CA-2011...   | 25.5   |
| Corporate    | Second Class     | CA-2012...   | 88.0   |
| ...          | ...              | ...          | ...    |

## ⚙️ How It Works

1. Reads the Excel file using `pandas`
2. Maps each segment to its corresponding columns
3. Loops through each ship mode and extracts:
   - Segment name
   - Ship mode
   - Order ID
   - Sales value
4. Stacks all segment/mode combinations into a single DataFrame
5. Cleans up invalid/missing sales entries
6. Exports the result to `sales_data_analyzed.xlsx`

## 🚀 How to Run

### 1. Install Pandas
```bash
pip install pandas

