Manufacturer entity matching

Inputs
	- Sunshine - Data/Outputs_Cleanup/Sunshine/pharmCo_info.csv
	- openfda - Data/Outputs_Cleanup/FDA/openfda_processsed.csv

Inputs modified to include only manufacturer_name (inputs generated from this notebook)
	(left_file)  Data/Outputs_Cleanup/Sunshine/pharmCo_info.csv  >> 
				 Data/Outputs_Cleanup/Sunshine/pharmCo_manufacturer_dedupe_input.csv
	
	(right_file) Data/Outputs_Cleanup/FDA/openfda_processsed.csv >> 
			 	 Data/Outputs_Cleanup/FDA/openfda_manufacturer_dedupe_input.csv

Outputs
	- Dedupe settings          - Data/Outputs_Cleanup/Manufacturer_entity_matching/
	- Dedupe training          - Data/Outputs_Cleanup/Manufacturer_entity_matching/
	- Dedupe matching output   - Data/Outputs_Cleanup/Manufacturer_entity_matching/
