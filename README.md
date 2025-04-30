Make directory to place manifest file in: 
mkdir tcga_LUSC_data_somatic_mutation

cd tcga_LUSC_data_somatic_mutation

Go to https://portal.gdc.cancer.gov/

Go to Projects and filter in Primary Site to bronchus and lung 

Save cohort and set as current. Then navigate to repository and Select these file types: 
Data Format  = maf (Select under Files tab)
Access = open
Data Type = Masked Somatic Mutation

Download manifest file and place in VM: 

Download gdc-client 

Next unpack all of files using this command but enter the manifest file name
gdc-client download -m [manifest_FILE_NAME]

Write bash loop to move all files in downloaded directories up in your parent directory. 


Next make bash script that uncompresses each file and counts the number of time STAT5A and TP53 appears. 
