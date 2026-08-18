## NHS A\&E Performance Analysis

### Project Description:



This project examines whether treatment delays in NHS emergency departments correlate with unplanned patient reattendances. It analyses operational performance across the NHS emergency care network, focusing on wait times, treatment speed, and 7-day return-visit rates, to identify which Trusts are under the most pressure and whether performance is improving or deteriorating.



### Data:
#### Source: 
NHS England Provisional A\&E Quality Indicators, December 2025 by Provider https://digital.nhs.uk/data-and-information/publications/statistical/provisional-accident-and-emergency-quality-indicators-for-england/december-2025-by-provider



### Three source files were used:



Core fact table — monthly KPI readings per organisation (long format)

KPI metadata — definitions and specifications for each measure

Trust reference table — organisation names, regions, and open/close status



After cleaning (removing closed Trusts and the national ENG aggregate row), the analysis covers 140 active NHS Trusts across 25 months (December 2023 – December 2025), totalling 78,386 records.



### Findings:

1. Blackpool Teaching Hospitals has the longest average A&E wait in the dataset, at 5 hours 52 minutes (352 minutes), 1 hour 23 minutes above the next-worst Trust (Wirral, 4 hours 29 minutes) and more than double the national median 169 minutes (2 hours 49 minutes).

2. National median A&E wait time improved from 3 hours 6 minutes in December 2023 to 2 hours 37 minutes in August 2024, and has held steady in a 2h39m–2h47m range since spring 2025.

3. 27 Trusts have reattendance rates above 10%, and treatment speed is not the cause. Northumbria Healthcare NHS Foundation Trust has one of the fastest treatment times in the dataset (37.3 minutes) but the highest reattendance rate (15.2%).



### Repository Structure:

    nhs-ae-analytics/

    README.md                        # Project overview and findings

    notebooks/

    01_data_preparation.ipynb        # Loads, cleans, and joins raw NHS data

    02_analysis.ipynb                # Derives KPIs and regional aggregations

    03_visualisation.ipynb           # Builds the 4 portfolio charts

    04_reporting.ipynb               # Generates the Excel report

    output/                          # Final Excel report and chart PNGs
  
    data/                            # Empty; raw CSVs excluded (see .gitignore)


### How to Run:

Download the three NHS England source files from the link above and place them in a local data/ folder (not committed to this repository — see .gitignore).

Open notebooks/01\_data\_preparation.ipynb in Google Colab, mount Google Drive, and set the file path constants at the top to match your own Drive structure.

Run all four notebooks in order:

01\_data\_preparation.ipynb — loads, cleans, and joins the three source files

02\_analysis.ipynb — derives performance metrics and regional aggregations

03\_visualisation.ipynb — generates the four portfolio charts

04\_reporting.ipynb — builds the final Excel report

Each notebook should be run top-to-bottom in a fresh session. Outputs from each stage are required by the next.



#### Author:
Husnain Zahoor

