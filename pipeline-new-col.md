# ➕ New Column – Volantis Pipeline

## Overview  
The Add New Column feature helps you create a custom column by using formulas, expressions, or functions based on your existing data. This feature is perfect for:

- Applying calculations like SUM, IF, AVG, and more.  
- Combining or modifying multiple columns into a new field. 
- Preparing new data for better analysis or visualization.  
- Keeping the original dataset safe and untouched.

By creating a new column, you can enhance your data without risking any changes to the original information.
---

## Configuration

![New Column Config](/vdata/documentation/pipeline/new-col/new-col-config.webp)

| Section          | Property       | Description                                                                 | Example               |
|------------------|----------------|-----------------------------------------------------------------------------|-----------------------|
| **Column Name**  | Custom Name    | Name of the new column to be created.                                       | `JUMLAH DATA`         |
| **Expression**   | Formula Field  | Calculation or function applied using column references and logic.          | `SUM(\`c_0:No\`)`     |

---

## Functions, Conditions, and Comparators

When creating expressions, you can use various built-in functions, conditional logic, and comparators. Here's a quick guide:

### Available Functions

Functions are mainly used to perform calculations within a single column.

| Function   | Description                                  | Example                            |
|------------|----------------------------------------------|------------------------------------|
| `SUM()`    | Adds all the values within one column.       | `SUM(`c_0:Sales`)`                 |
| `AVG()`    | Calculates the average of all values in a column. | `AVG(`c_0:Score`)`             |
| `MIN()`    | Returns the smallest value found in a column. | `MIN(`c_0:Price`)`                |
| `MAX()`    | Returns the largest value found in a column. | `MAX(`c_0:Temperature`)`           |

> **Note:** When using `SUM()`, `AVG()`, `MIN()`, or `MAX()`, it usually calculates the result across the values of a single column unless combined explicitly with other columns.

### Conditions

Conditions help control the output based on specific rules using IF().

  ```text
  IF(
    `c_12:Document Type` == "Invoice"
    || `c_12:Document Type` == "Tax Invoice"
    || `c_12:Document Type` == "Contract"
    || `c_12:Document Type` == "Company Owner's ID"
    || `c_12:Document Type` == "Receipt"
    || `c_12:Document Type` == "Non-Taxable Company Letter"
  ) RETURN `c_12:Document Type`
  ELSE RETURN "Other Documents"
  ```

### Comparators

Comparators are used to compare values inside expressions.

| Comparator | Meaning                  | Example                        |
|------------|---------------------------|--------------------------------|
| `==`        | Equal to                  | `c_0:Status` = 'Active'         |
| `!=`       | Not equal to               | `c_0:Status` != 'Inactive'      |
| `>`        | Greater than               | `c_0:Sales` > 5000              |
| `<`        | Less than                  | `c_0:Quantity` < 10             |
| `>=`       | Greater than or equal to   | `c_0:Score` >= 80               |
| `<=`       | Less than or equal to      | `c_0:Discount` <= 20            |

You can combine these comparators inside `IF()` or other functions.

### Arithmetic Operators

You can use arithmetic operators to perform calculations between columns or numeric values.


| Operator   | Description               | Example                        |
|------------|---------------------------|--------------------------------|
| `+`        | Addition                  | `c_0:Status` = 'Active'         |
| `-`        | Subtraction               | `c_0:Status` != 'Inactive'      |
| `*`        | Multiplication            | `c_0:Sales` > 5000              |
| `/`        | Division                  | `c_0:Quantity` < 10             |
| `**`       | Exponentiation            | `c_0:Score` >= 80               |


---

## Previewing the Output

![New Column Preview](/vdata/documentation/pipeline/new-col/new-col-prev.webp)

Use the **Preview** button to ensure:

- Your expression is valid and returns the expected result.  
- Aggregated values appear as intended.  
- The new column looks correct beside the original data.
- Click **Save** to apply the transformation.