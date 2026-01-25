# BS-EN-15804-impacts-considering-grid-decarbonisation-trajectories
Open source Python tool for calculating environmental impacts in accordance with BS EN 15804:2012+A2:2019, enabling assessment of materials manufactured in future accounting for grid decarbonisation pathways. The tool currently supports forecast data from:

- National Grid ESO, Future Energy Scenarios, (2023). https://www.neso.energy/data-portal/regional-breakdown-fes-data-electricity (accessed July 25, 2022).
- European Commission, POTEnCIA Central-2018 scenario, Joint Research Centre (JRC) [Dataset], (2024). http://data.europa.eu/89h/3182c195-a1fc-46cf-8e7d-44063d9483d8 (accessed January 8, 2026).
- European Commission, POTEnCIA CETO 2025 Scenario - European Commission, Joint Research Centre (JRC) [Dataset], (2025). https://data.jrc.ec.europa.eu/dataset/1d9562ad-b342-498c-b34e-50ac04b00ded (accessed January 8, 2026).
- IEA, Energy Projections of IEA Countries – National Data, IEA (2025). https://www.iea.org/data-and-statistics/data-product/iea-statistics-package-isp-2 (accessed January 8, 2026). For this dataset a license is required. 
- IEA, World Energy Outlook 2025 Dataset, IEA (2025). https://www.iea.org/data-and-statistics/data-product/world-energy-outlook-2025-free-dataset (accessed January 8, 2026).

Workflow:
1. Download the complete "Future_impacts_calculator" folder and store it locally in "Downloads", e.g. /Users/yourname/Downloads/Future_impacts_calculator
2. The dataset from "IEA, Energy Projections of IEA Countries – National Data, IEA (2025)" is not included in the abovementioned folder. The user will have to obtain the data through: https://www.iea.org/data-and-statistics/data-product/iea-statistics-package-isp-2 (a license is required)
3. Using SimaPro, calculate all Ecoinvent High Voltage electricity market country mixes in MJ. This includes every available dataset of the form
"Electricity, high voltage {CN}| market group for electricity, high voltage | Cut-off, U". Extract the results for all BS EN 15804:2012+A2:2019 impact categories and paste them into the “Countries electricities” sheet of the provided "Impacts to subtract.xlsm" Excel file. These data are not supplied with the tool
4. Using SimaPro, calculate all Ecoinvent electricity by fuel in MJ (e.g. Gas, Nuclear, Wind etc.). This includes every available dataset of the form "Electricity, high voltage {CN-GS}| electricity production, natural gas, conventional power plant | Cut-off, U". Extract the results for all BS EN 15804:2012+A2:2019 impact categories and paste them into the relevant sheets of the "Impacts per MJ of technology inventory" Excel file.

For the material to be analysed, export the process contribution inventory from SimaPro using default units
1. Paste the exported data into cell A1 of "Paste results here" sheet in "impacts to subtract.xlsx" spreadsheet.
2. Save the spreadsheet
3. Run the python script, select the desired grid decarbonisation pathway and the year the material is to be manufactured
4. Environmental impacts of materials manufactured in future can be found in "Future_Impacts_Results.xlsx"

Details on the pathways and scenario mapping are provided in the associated publication:

Kordilas M, Mumovic D, Schwartz Y, et al (2025) Temporal myopia in building Life Cycle Assessment? High resolution versus coarse dynamics in climate change and grid decarbonisation [under review]. Building and Environment

IEA World Energy Outlook Free Dataset is used under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 license (CC BY-NC-SA 4.0)
ISO 3166 country codes can be accessed here https://www.iso.org/obp/ui/#search
Ecoinvent geographies file can be accessed here https://support.ecoinvent.org/geographies
