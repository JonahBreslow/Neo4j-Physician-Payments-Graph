# DSE-203-Knowledge-Graph

## Dataset Ideas
### Open Payments & Drug PrescriptionsTT40.
1. CMS Open Payments (Sunshine act) [Data](https://openpaymentsdata.cms.gov/datasets?sort=modified)
2. Part D prescriptions [Data](https://data.cms.gov/provider-summary-by-type-of-service/medicare-part-d-prescribers/medicare-part-d-prescribers-by-provider-and-drug/data/2019)
3. CDC Deaths by Type by Month and Year and State [Data](https://data.cdc.gov/NCHS/VSRR-Provisional-Drug-Overdose-Death-Counts/xkb8-kh2a/)
4. [Lucid Chart Graph POC](https://lucid.app/lucidchart/e4d591c7-a579-4043-903f-c08cebcb67b1/edit?viewport_loc=-11%2C-11%2C1571%2C876%2C0_0&invitationId=inv_f837e136-888d-478a-a245-304858e2eff7)

### Questions:
1. How does money affect prescription rates. Do doctors that receive money from pharmaceutical companies presecribe more that/those company's drugs?
2. Is there a similar relationship in regards to the hospital and pharmaceutical companies
3. Is there a link between how much in total pharmaceutical companies spend in a state and that state's opiod death rate/count?

## Data Descriptions:

### CMS Open Payments(Sunshine Act)
1. Covers period 2013 to 2020. Covers the whole year in each period
2. 3 Types of Payments:
   - General Payments
   - Research Payments
   - Ownership Payments
3. Each type of sheet includes information:
   - Receiving institution or doctor
   - Purpose of payment
   - Paying insitution or person
### Part D Prescriptions
1. Data Methodolgy:
>The Medicare Part D Prescribers by Provider and Drug dataset provides information on prescription drugs prescribed to Medicare beneficiaries enrolled in Part D >by physicians and other health care providers. This dataset contains the total number of prescription fills that were dispensed and the total drug cost paid >organized by prescribing National Provider Identifier (NPI), drug brand name (if applicable) and drug generic name."
2. Columns:
   - Prescriber Data (Name, NPI, City, State, Specialty)
   - Drug Data (Brand, USAN Generic Name - Short Version)
   - Prescription Data (Number of Medicare Part D Claims, Including Refills, Number of Standardized 30-Day Fills, Including Refills, Number of Day’s Supply for All Claims, Aggregate Cost Paid for All Claims, Aggregate Cost Paid for All Claims, etc.)


### CDC Deaths
1. Covers period April 2015 to March 2021.
2. Data is shown as 12-month period ending in a particular month. So 12 month period ending in July 2021 will cover the period Aug 1,2020 to July 31,2021
3. Covers all 50 states and District of Columbia
4. Will focus on cause called Opiods(T40.0-T40.4,T40.6)
   - T40.0: Opium.
   - T40.1: Heroin.
   - T40.2: Natural opioid analgesics, including morphine and codeine, and semisynthetic opioids, including drugs such as oxycodone, hydrocodone, hydromorphone, and oxymorphone.
   - T40.3: Methadone
   - T40.4: Synthetic opioid analgesics other than methadone, including drugs such as fentanyl and tramadol.
   - T40.6: Other and unspecified narcotics
