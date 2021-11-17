Data Link: https://data.cdc.gov/NCHS/VSRR-Provisional-Drug-Overdose-Death-Counts/xkb8-kh2a/
## Information
1. 41626 Rows
2. 12 Columns
## Columns
1. State
    - AK: Alaska, AL: Alabama, AR: Arkansas, AZ: Arizona, CA: California, CO: Colorado, CT: Connecticut,
    - DC: District of Columbia, DE: Delaware, FL: Florida, GA: Georgia, HI: Hawaii, IA: Iowa, ID: Idaho,
    - IL: Illinois, IN: Indiana, KS: Kansas, KY: Kentucky, LA: Louisiana, MA: Massachusetts, MD: Maryland,
    - ME: Maine, MI: Michigan, MN: Minnesota, MO: Missouri, MS: Mississippi, MT: Montana, NC: North Carolina,
    - ND: North Dakota, NE: Nebraska, NH: New Hampshire, NJ: New Jersey, NM: New Mexico, NV: Nevada, NY: New York,
    - OH: Ohio, OK: Oklahoma, OR: Oregon, PA: Pennsylvania, RI: Rhode Island, SC: South Carolina, SD: South Dakota,
    - TN: Tennessee, TX: Texas, US: United States, UT: Utah, VA: Virginia, VT: Vermont, WA: Washington, 
    - WI: Wisconsin, WV: West Virginia, WY: Wyoming, YC: New York City
2. Year
    - 2015 - 2021
3. Month
    - January - December
4. Period
    - 12 Month ending
    - This means the sum of the 12 months prior to the month stated in column 3
5. Indicator
    - 12 Unique Values
    - If label lists multiple codes then it is combination of each of the codes.
    - Natural, semi-synthetic, & synthetic opioids, incl. methadone (T40.2-T40.4)
    - Natural & semi-synthetic opioids (T40.2)
    - Natural & semi-synthetic opioids, incl. methadone (T40.2, T40.3)
    - Number of Deaths (Aggregated Number)
      - From all sources combined not just drugs
    - Opioids (T40.0-T40.4,T40.6)
    - Cocaine (T40.5)
    - Synthetic opioids, excl. methadone (T40.4)
    - Psychostimulants with abuse potential (T43.6)
    - Heroin (T40.1)
    - Percent with drugs specified (Aggregated Number)
    - Number of Drug Overdose Deaths (Aggregated Number)
    - Methadone (T40.3)
6. Data Value
    - Lots of missing values
7. Percent Complete
    - If counts are complete and all investigation into the deaths concluded
8. Percent Pending Investigation
9. State Name
10. Footnote
    - Numbers may differ from published reports using final data. See Technical Notes.  Data not shown due to low data quality.
    - Numbers may differ from published reports using final data. See Technical Notes.
    - Numbers may differ from published reports using final data. See Technical Notes.  Data suppressed (<10).  Data not shown due to low data quality.
    - Numbers may differ from published reports using final data. See Technical Notes.  Data suppressed (<10).
    - Underreported due to incomplete data.
    - Underreported due to incomplete data.  Data suppressed (<10).
    - Underreported due to incomplete data.  Data not shown due to low data quality.
    - Underreported due to incomplete data.  Data suppressed (<10).  Data not shown due to low data quality.
11. Footnote Symbol
    - *, **
12. Predicted Value
    - Some values match that in column Data Value
## Data Cleanup Procedures
We need to remove as many missing values from the "Data Values" column as possible. 
We can use the column Predicted Value to fill in the blanks
1. If Data Value is Blank:
    - If Predicted Value is not blank:
        - Use that value
    - Else
        - Use average of value in previous time frame and next time frame
        - This is going off the fact that the data values are listed as the sum of the last 12 months so the value for a particular month if missing should be the difference between the next month and the previous month.
        - We cannot use the whole difference though because some value is from the following month so taking an average is the most fair.
## Nodes and Edges
:Deaths{value : data.Values}<br>
:Month{month : data.Month}<br>
:Year{year : data.Year}<br>
:DeathType{type : data.Indicator}<br>
:State{state : data.State}<br>
--------------------------------------<br>
( :Deaths )-[ :OF_TYPE]->( :DeathType )<br>
( :Deaths )-[ :LOCATED_IN]->( :State )<br>
( :Deaths )-[ :OCCURED_IN]->( :Month )<br>
( :Month )-[ :OF]->( :Year )<br>
## Load Statement
