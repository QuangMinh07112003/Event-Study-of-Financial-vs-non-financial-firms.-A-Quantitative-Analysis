# Event Study of Financial vs Non-Financial firms

### Hazel Choe & Minh Trinh

## Description

This project focuses on understanding how asset management companies and consumer staples companies, both large-cap(big) and small-cap(small), have been influenced by a financially driven crisis and an operationally driven crisis, using both the 2008 GFC (Global Financial Crisis) and the 2020 COVID-19 crises. The goal is to understand how firms provide asset management services, and those that fall within the consumer staples industry have been influenced by both types of crisis.

## Data Retrieval

### Primary Dataset: Crisis_Impact_2008 & Crisis_Impact_2020

- Both scraped from companiesmarketcap.com (publicly available)
- To check the credibility of this data, we checked the values manually from Yahoo Finance.

## Data Overview

After cleaning and preprocessing, we used these two primary datasets for each crisis event in 2008 & 2020. Each processed dataset contains:

- Companies (Big / Small)
- Revenue
- YoY revenue growth
- Demand Effect
- Operational Effect
- Sector (Asset management / Consumer staples)
- Size based on each sector
- Fama-French 5 factor coefficients
- Firms' daily returns (from 'yfinance' library)

## Libraries

The following Python libraries are required to run the analysis and modeling process:

``` python
from selenium import webdriver
from selenium.webdriver.common.by import By
import pandas as pd
import time
import re
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import yfinance
import statsmodels.api as sm
```

## Methodology

These metrics are linked to stock return behavior to see whether firms with stronger operational fundamentals stock more effectively.

- YoY revenue growth
- Demand effect
- Operational effect
- Firm size

## Visualization

### Revenue Growth Shock Heatmap 2008 & 2020
   
<img width="1615" height="1982" alt="heatmap_2008" src="https://github.com/user-attachments/assets/d1dbeb96-4bac-4b8d-850c-f9238a1c7346" />
<img width="1620" height="2097" alt="heatmap_2020" src="https://github.com/user-attachments/assets/52c1060a-1ced-4bc4-9f7a-ba8599bd3d28" />

### Operational Effect by Firm 2008 & 2020

<img width="2612" height="1634" alt="operational_effect_2008" src="https://github.com/user-attachments/assets/25a8aaf6-d5cd-4ae1-932a-8a060fb045c2" />
<img width="2624" height="1634" alt="operational_effect_2020" src="https://github.com/user-attachments/assets/8d62ef46-ed2c-4f6d-b2b6-bbda1999e225" />

### Crisis Impact 2008 & 2020

<img width="4413" height="1468" alt="fundamentals_fingerprint" src="https://github.com/user-attachments/assets/c7cd8929-c84b-4b75-b20b-821e12210a23" />

### Cumulative Abnormal Returns (2008 Financial Crisis)
<img width="1172" height="701" alt="image" src="https://github.com/user-attachments/assets/2d6b9c8f-b052-4d2e-811e-b55bcf201d28" />
<img width="1181" height="701" alt="image" src="https://github.com/user-attachments/assets/b960697d-6610-4821-b01d-26e0e9d65d84" />

### Cumulative Abnormal Returns (COVID-19 pandemic)

<img width="1200" height="701" alt="image" src="https://github.com/user-attachments/assets/e5245872-310c-44f9-9e2b-147f58cf56cc" />
<img width="1200" height="701" alt="image" src="https://github.com/user-attachments/assets/d8ebb0bb-e944-4cbe-af60-8e9b1b92f032" />





## Citations

- Comparing COVID-19 with the GFC (currency markets): https://pmc.ncbi.nlm.nih.gov/articles/PMC9756040/
- Global Recovery (GFC vs. COVID-19): https://www.conference-board.org/publications/a-different-kind-of-global-recovery
- Fama/French 5 Factors (2x3): https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html

