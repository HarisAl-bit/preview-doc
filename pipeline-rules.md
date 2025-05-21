# 📜 Rules – Volantis Pipeline

## Overview  
The **Rules** feature enables filtering of rows based on conditions. It helps you:

- Segment your dataset  
- Focus on relevant subsets  
- Prepare data for analysis or visualization  
- Apply logic-based filtering with multiple conditions

---

## Configuration

![Rules Config](/vdata/documentation/pipeline/rules/rules-config.webp)

| Section            | Property                  | Description                                                                 | Example             |
|--------------------|---------------------------|-----------------------------------------------------------------------------|---------------------|
| **Add Rule**       | Column, Operator, Value   | Define the filtering logic using field comparison.                         | `Pendapatan >= 1300`|
| **Logical Connect**| AND / OR                  | Link multiple rules using logical relationships.                           | `AND`, `OR`         |
| **Operator**       | =                         | Equal to                                                                   | -                   |
|                    | !=                        | Not equal to                                                               | -                   |
|                    | >                         | Greater than                                                               | -                   |
|                    | <                         | Less than                                                                  | -                   |
|                    | >=                        | Greater than or equal to                                                   | -                   |
|                    | <=                        | Less than or equal to                                                      | -                   |


---

## Previewing the Output

![Rules Preview](/vdata/documentation/pipeline/rules/rules-preview.webp)

Use the **Preview** button to:

- See the rows that match your defined conditions  
- Validate that filters are applied as intended  
- Spot-check whether combined rules (AND/OR) work correctly  
- Ensure only relevant data will remain

Previewing helps avoid errors before saving the transformation.