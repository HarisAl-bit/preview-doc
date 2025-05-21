# 🧮 Scorecard Widget

## Overview

The Scorecard Widget displays a single numeric value with optional styling such as title, background, and formatting. It is often used to highlight key metrics or KPIs in a compact, visually focused format.

---

## Configuration

![Scorecard config](/vdata/documentation/xplorer/scorecard/scorecard-config.webp)

| Property | Description                              | Example        |
|----------|------------------------------------------|----------------|
| **Value** | Numeric field to display in the card.   | `Total Sales`  |

---

## Style

- ### **Scorecard Title Settings**

![Scorecard Title](/vdata/documentation/xplorer/scorecard/scorecard-title.webp)  

| Property  | Description                          | Example       |
|-----------|--------------------------------------|---------------|
| Position  | Alignment of the title text.         | `Top Center`  |
| Size      | Font size of the title.              | `24px`        |
| Color     | Title text color.                    | `#000000`     |

---

- ### **Card Style Settings**

![Scorecard Card Style](/vdata/documentation/xplorer/scorecard/scorecard-cardstyle.webp)  

| Property      | Description                               | Example      |
|---------------|-------------------------------------------|--------------|
| Border Style  | Style of card border (`None`, `Solid`, etc.). | `None`   |
| Width         | Thickness of card border.                 | `0px`        |
| Color         | Color of the card border.                 | `#000000`    |
| Background    | Background color of the card.             | `#FFFFFF`    |

---

- ### **Score Style Settings**

![Scorecard Style](/vdata/documentation/xplorer/scorecard/scorecard-scorestyle.webp)  

| Property      | Description                               | Example        |
|---------------|-------------------------------------------|----------------|
| Score Weight  | Font weight of the main number.           | `Medium`       |
| Size          | Font size of the score number.            | `32px`         |
| Color         | Text color of the score number.           | `#00FF00`      |
| Prefix        | Character/text before the number.         | `$`            |
| Digit         | Number of decimal digits to display.      | `0`            |
| Suffix        | Character/text after the number.          | `%`, `items`   |


