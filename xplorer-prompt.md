# 💬 Prompt Widget

## Overview

The **Prompt Widget** allows users to input natural language queries or instructions that are interpreted by the system using the connected dataset. It is designed for interactive data exploration and AI-powered insights.

---

## Configuration

![Prompt Config](/vdata/documentation/xplorer/prompt/prompt-config.webp)

| Property       | Description                                                       | Example                        |
|----------------|-------------------------------------------------------------------|--------------------------------|
| **Data Source** | Dataset used to provide context for the prompt.                   | `pivot_data_100rows`           |
| **Prompt**     | Natural language input to analyze or summarize data.              | `Analyze this raw data and provide...` |
| **Send Button**| Button to execute the prompt against the selected dataset.        | `Send`                         |

---

## Style

![Prompt Style](/vdata/documentation/xplorer/prompt/prompt-style.webp)

| Section         | Property        | Description                                      | Example         |
|----------------|------------------|--------------------------------------------------|-----------------|
| **Text Style**  | Font Weight      | Font weight of the prompt text.                  | `Normal`        |
|                 | Size             | Font size of the prompt text.                    | `14px`          |
|                 | Color            | Text color of the prompt.                        | `#000000`       |
|                 | Text Align       | Alignment of the text inside the widget.         | `Center`        |
| **Card Style**  | Border Style     | Card border style (`None`, `Solid`, etc.).       | `None`          |
|                 | Width            | Thickness of the card border.                    | `0px`           |
|                 | Color            | Color of the card border.                        | `#000000`       |
|                 | Background       | Card background color.                           | `#FFFFFF`       |

