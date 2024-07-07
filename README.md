"""
    input_file_name (str): Input JSON file name
    output_file_name (str): Output CSV file name
    input_column_name (str): Filter input file based on the columns
    output_column_name (list): Rename input columns. None by default. Note: Passing 'None' will keep the same column names
    index (bool): Toggle index in output file. False (turned off) by default
    """

    . Create a CSV data file for each table.
1. You will prepare a CSV file to collect data for each table in the schema of your design. For this, you can use create_dataset.py to collect the attributes for a table. The attribute names are those used in the original json files, e.g., id, name, position. Use a “path” to name an attribute that
2. is nested in the original json files, e.g., keywords.id, keywords.name, keywords.score. Note that this step can
         
Usage:
$ python3 create_dataset.py <path_json_file> <output_file> <attribute list>
Example: The following example extracts the columns id and researchInterest from faculty.json and writes it to csv file test1.csv.
$ python3 create_dataset.py faculty.json test1.csv "id, researchInterest"
