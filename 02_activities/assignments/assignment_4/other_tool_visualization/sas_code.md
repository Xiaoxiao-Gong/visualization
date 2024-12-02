# SAS Code for Data Visualization: Hospitalizations by Vaccination Status

This SAS script processes and visualizes hospitalizations data based on vaccination status. The dataset is imported, cleaned, transformed, and visualized to reveal trends in ICU and Non-ICU admissions.

```sas
libname d '/home/u61834617/dsi_project';

PROC IMPORT DATAFILE="/home/u61834617/dsi_project/Hospitalizations by vaccination status.csv"
    OUT=d.hospitalizations
    DBMS=CSV
    REPLACE;
    GETNAMES=YES;
RUN;

PROC PRINT DATA=d.hospitalizations (OBS=10);
RUN;

DATA d.hospitalization_summary;
    SET d.hospitalizations;
    total_icu = icu_unvac + icu_partial_vac + icu_full_vac;
    total_non_icu = hospitalnonicu_unvac + hospitalnonicu_partial_vac + hospitalnonicu_full_vac;
RUN;

PROC PRINT DATA=d.hospitalization_summary (OBS=10);
RUN;

DATA d.hospitalization_long;
    SET d.hospitalization_summary;
    LENGTH group $20 type $20;
    group = "Unvaccinated"; type = "ICU"; count = icu_unvac; OUTPUT;
    group = "Partially Vaccinated"; type = "ICU"; count = icu_partial_vac; OUTPUT;
    group = "Fully Vaccinated"; type = "ICU"; count = icu_full_vac; OUTPUT;
    group = "Unvaccinated"; type = "Non-ICU"; count = hospitalnonicu_unvac; OUTPUT;
    group = "Partially Vaccinated"; type = "Non-ICU"; count = hospitalnonicu_partial_vac; OUTPUT;
    group = "Fully Vaccinated"; type = "Non-ICU"; count = hospitalnonicu_full_vac; OUTPUT;
RUN;

PROC PRINT DATA=d.hospitalization_long (OBS=15);
RUN;

PROC SGPLOT DATA=d.hospitalization_long;
    VBAR date / RESPONSE=count GROUP=group GROUPDISPLAY=STACK;
    TITLE "Daily Hospitalizations by Vaccination Status";
    XAXIS LABEL="Date";
    YAXIS LABEL="Number of Admissions";
    KEYLEGEND / TITLE="Vaccination Status";
RUN;

PROC OPTIONS OPTION=WORK;
RUN;

PROC SGPANEL DATA=d.hospitalization_long;
    PANELBY type / NOVARNAME;
    VBAR date / RESPONSE=count GROUP=group GROUPDISPLAY=STACK;
    TITLE "Daily Hospitalizations by Vaccination Status and Type";
    ROWAXIS LABEL="Number of Admissions";
    COLAXIS LABEL="Date" FITPOLICY=THIN;
    KEYLEGEND / TITLE="Vaccination Status";
RUN;
