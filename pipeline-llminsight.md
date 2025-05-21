# 🧠 LLM Insight – Volantis Pipeline

## Overview  
**LLM Insight** is an AI-powered feature in Volantis Pipeline that uses Large Language Models (LLMs) to analyze tables and extract valuable insights automatically or through user-defined prompts.

With this feature, you can:  
- Generate **summary tables** from any dataset  
- Ask **custom questions** related to the data  
- Get answers in **structured table format**, perfect for analysis or reporting  

---

## Configuration

![LLM Insight Preview](/vdata/documentation/pipeline/llm-insight/llm-insight-config.webp)

| Field           | Description                                                                 | Example                                      |
|----------------|-----------------------------------------------------------------------------|----------------------------------------------|
| **Auto Summary** | By default, LLM Insight automatically creates a summary table based on the dataset provided. | _No input required_                         |
| **Custom Prompt** | Optional prompt to guide the AI to extract specific information from the table. | `What is the highest expenditure?`          |
| **Save Config**   | Button to store your settings before executing the pipeline.               | _Click to save prompt and config_           |

### Notes:
- Prompts must be written in **English** for optimal results.
- The AI is designed to handle natural language questions and return useful insights.

---

## Preview  

Below is a visual representation of how the **LLM Insight** component looks in the Volantis UI:

![LLM Insight Preview](/vdata/documentation/pipeline/llm-insight/llm-insight-preview.webp)

### Example Output (Tabular Format):

| Category     | Expenditure |
|--------------|-------------|
| Marketing    | $125,000    |
| Operations   | $98,500     |
| Logistics    | $76,200     |

LLM Insight will always return output in **table format**, making it easier to interpret and export.

---

