# DATA VALIDATOR

Data Validator is a framework which is used to compare data of two database tables or custom SQL outputs for cell mismatches

## USE CASES

Data comparison between source and target objects.

While migrating data of a project. 

integrate DVM report in pipeline for Cell by cell mismatches.

## DVM Config File: - 

### DVM Config File Tags 

1. Name: -                         Name for the testcase 

2. Category: -                     Category in which we want to run our testcase 

3. Run_flag:-                      Y if you want to run our testcase else N 

4. Db_config_path:-                Path for the dB credentials file(config.conf), Path can be                   relative or absolute 

5. Type: - 		                   Give the type of testcase like DVM, gempyp etc. 

6. DataBase:-                      Give the type of dataBase like MySQL 

7. Source_db:-                     Which credentials or schema do we want to use in our testcase    		from config file for source_sql like source1, source2 

8. Target_db:-                     Which credentials or schema do we want to use in our testcase from config file for target_sql like target1, target2 

9. Source_sql:-                    SQL query we want to run in sourceDB to fetch data 

10. Target_sql:-                   SQL query we want to run in targetDB to fetch data 

11. Keys: -                        Column we want to use as key in our testcase, we can have   		           multiple commas separated keys 

12. Threshold: -                   Number of values we want after decimal in our testcase 

### Config.conf File

Config.conf file contains the credentials which are required to make connections with the database. We can have multiple setups of the credentials in blocks for different testcases 

In conf file we have to specify several terms: - 

1. [DB Credentials Name]                    Need in XML file to find which DB is to use

2. Host: -                                  Host name for the database 

3. DatabaseName:-                           Name of the database with which we want to connect 

4. User: -                                  Specify the type of user 

5. Password: -                              Password required for database connection 

We can have multiple of these kind of DB credentials in our config file
Note: Every db credentials should have different name

### How to run Data Validator?

Create config.conf file as mentioned

Create an XML file having above mentioned tags in <testcase> and give relative or absolute path for config.conf file in <db_config_path> tag

Testcase type should be DVM in tag <type>

### Command to run Data Validator?

Give command ---  gempyp -c path/to/xmlfile 

### Sample Report

Jewel: https://jewel.gemecosystem.com/#/autolytics/extent-report?s_run_id=GEMECO-API-PY-DVM_PROD_3FD571D7-5D99-4DC6-B8D8-F6CB37668BF7

### Sample Excel File

In execl folder excel file related to testcases are present