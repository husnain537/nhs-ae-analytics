NHS A\&E Performance Analysis

Project Description:



This project examines whether treatment delays in NHS emergency departments correlate with unplanned patient reattendances. It analyses operational performance across the NHS emergency care network, focusing on wait times, treatment speed, and 7-day return-visit rates, to identify which Trusts are under the most pressure and whether performance is improving or deteriorating.



Data:



Source: NHS England Provisional A\&E Quality Indicators, December 2025 by Provider https://digital.nhs.uk/data-and-information/publications/statistical/provisional-accident-and-emergency-quality-indicators-for-england/december-2025-by-provider



Three source files were used:



Core fact table — monthly KPI readings per organisation (long format)

KPI metadata — definitions and specifications for each measure

Trust reference table — organisation names, regions, and open/close status



After cleaning (removing closed Trusts and the national ENG aggregate row), the analysis covers 140 active NHS Trusts across 25 months (December 2023 – December 2025), totalling 78,386 records.



Findings:

Blackpool Teaching Hospitals has the longest average A\&E wait in the dataset, at 352 minutes — 83 minutes above the next-worst Trust (Wirral, 269 minutes) and more than double the national median (169 minutes).

National median A\&E wait time improved from 186 minutes in December 2023 to 157 minutes in August 2024, and has held steady in a 159–167 minute range since spring 2025.

27 Trusts have reattendance rates above 10%, and treatment speed is not the cause. Northumbria Healthcare NHS Foundation Trust has one of the fastest treatment times in the dataset (37.3 minutes) but the highest reattendance rate (15.2%).



Repository Structure:

nhs-ae-analytics/

&#x20; README.md

&#x20; .gitignore

&#x20; notebooks/

&#x20;   01\_data\_preparation.ipynb

&#x20;   02\_analysis.ipynb

&#x20;   03\_visualisation.ipynb

&#x20;   04\_reporting.ipynb

&#x20; output/

&#x20;   NHS\_AE\_Report.xlsx

&#x20;   chart\_top10\_wait\_time.png

&#x20;   chart\_england\_trend.png

&#x20;   chart\_treatment\_vs\_reattendance.png

&#x20; data/

&#x20;   .gitkeep



How to Run:

Download the three NHS England source files from the link above and place them in a local data/ folder (not committed to this repository — see .gitignore).

Open notebooks/01\_data\_preparation.ipynb in Google Colab, mount Google Drive, and set the file path constants at the top to match your own Drive structure.

Run all four notebooks in order:

01\_data\_preparation.ipynb — loads, cleans, and joins the three source files

02\_analysis.ipynb — derives performance metrics and regional aggregations

03\_visualisation.ipynb — generates the four portfolio charts

04\_reporting.ipynb — builds the final Excel report

Each notebook should be run top-to-bottom in a fresh session. Outputs from each stage are required by the next.



Author:
Husnain Zahoor

