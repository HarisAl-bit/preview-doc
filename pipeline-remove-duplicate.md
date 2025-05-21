# 🧹 Remove Duplicate – Volantis Pipeline

## Overview  
The **Remove Duplicate** feature helps you clean your dataset by removing redundant rows based on selected columns.

---

## Configuration

![Remove Duplicate Config](/vdata/documentation/pipeline/remove-duplicate/remove-duplicate-config.webp)

| Section            | Property       | Description                                                               | Example            |
|--------------------|----------------|---------------------------------------------------------------------------|--------------------|
| **Select Columns** | Multi-select   | Columns used to identify duplicate rows (based on identical values).      | `Email Address`    |

> ⚠️ Only the **first occurrence** of a duplicate is retained. Others are discarded.

---

## Previewing the Output

![Remove Duplicate Preview](/vdata/documentation/pipeline/remove-duplicate/remove-duplicate-preview.webp)

Use the **Preview** button to:

- Check which rows will be removed before applying the transformation  
- Verify that the intended columns are correctly identifying duplicates  
- Ensure the retained rows match your expectations

This helps prevent accidental data loss and gives visibility into how your data will be cleaned.
