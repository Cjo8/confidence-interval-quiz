# 95% Confidence Interval Quiz

## TL;DR

A lightweight Python/Flask app that tests real-world understanding of 95% confidence intervals.  
Users enter lower/upper bounds for 20 questions, get instant scoring + interpretation, and see global accuracy stats.  
Built with Flask, Bootstrap, JSON persistence, and deployed on Railway with a custom domain.  
Demonstrates behavioral-science application, uncertainty calibration, UX flow design, and full-stack implementation.

## Full Description

A simple web application that tests how well people understand **95% confidence intervals**. For each of 20 questions, users enter a **lower** and **upper** bound they believe contains the true value 95% of the time. The app scores accuracy, provides interpretation, and aggregates anonymized global correctness statistics across all completions.

## What This Is

This quiz gives users a practical sense of what *true* statistical confidence looks like. Most people are dramatically overconfident, choosing intervals far too narrow. This tool reveals that bias and helps calibrate intuition.

Features:

- 20-question interval-estimation quiz  
- Dynamic progress bar  
- Real-time scoring  
- Results page with calibration interpretation  
- Persistent global correctness averages (`stats.json`)  
- Clean, minimal Bootstrap-based UI

## Why Confidence Intervals Matter

The **95% confidence interval (CI)** is one of the core tools in scientific research. It reflects the range within which the true value would fall in roughly 95 out of 100 repeated samples.

Because people underestimate uncertainty, confidence intervals chosen by individuals are usually far too narrow—a result replicated across psychology, economics, forecasting, and decision science.

This quiz makes that gap visible.

**Example:**  
When Pfizer published the first randomized trial results for the COVID-19 vaccine, the widely cited “**95% effective**” number was based directly on the 95% confidence interval calculated from **170 confirmed cases** detected in a **43,000-participant** study.

Source:  
CNBC — “Pfizer says final data analysis shows Covid vaccine is 95% effective”  
https://www.cnbc.com/2020/11/18/coronavirus-pfizer-vaccine-is-95percent-effective-plans-to-submit-to-fda-in-days.html

---

## Live Demo
**https://ciquiz.systemii.co/**  
Deployed via **Railway** with automatic GitHub deployments.


---

## Tech Stack

- **Python**
- **Flask**
- **HTML / CSS / Bootstrap**
- **JSON** (lightweight global stats persistence)
- **Gunicorn** (production server)
- **Railway** (deployment platform with custom domain)

---

## Project Structure
- app.py
- requirements.txt
- Procfile
- static/
- templates/
- stats.json
- .gitignore

---

## Running Locally
### 1. Clone the repo

    ```bash
    git clone https://github.com/tatmanta/confidence-interval-quiz.git
    cd confidence-interval-quiz
    ```

### 2. Create and activate a virtual environment
#### macOS / Linux:
        ```bash
        python -m venv venv
        source venv/bin/activate
        ```

#### Windows (PowerShell or CMD):
        ```bash
        python -m venv venv
        venv\Scripts\activate
        ```

### 3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

### 4. Run the app:
    ```bash
    python app.py
    ```

### 5. Open in browser:
    http://127.0.0.1:5000
