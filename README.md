# ETL_From_GiTHub_To_Azure_PGAdminPGAdmin4
1. Fork from GitHub
The extract part of the code has been taken care of, so you just need to focus on the main.py file.

You need to create a Python function that takes a Pandas DataFrame as input and performs the following transformations:

Iterate through each column name.
Convert the column name to lowercase.
Replace any spaces in the column name with underscores (_).
Example: "Time Uploaded" becomes "time_uploaded".

Access the "reading_time" column.
For each value in the column, remove the string " min read" from the end.
Ensure that the remaining value in the column is converted to the appropriate datatype, probably an integer.

Access the "article_content" column.
For each value in the column, replace all occurrences of the newline character (\n) with an empty string ("").

After the transformations, ensure that each column has the correct data type (e.g., integer, string, date, etc.). 
You might need to use Pandas functions like astype() to enforce these data types.
Determine the appropriate data types for each column based on the data that it contains.

Open pgAdmin.
Create a new server connection using the provided credentials:

Host: your_host
Port: your_port
Database: postgres
Username: your_username
Password: your_password

In the connected database, create a new table with your name (e.g., yourname).
Define the columns with appropriate data types:

The link column must be defined as the primary key.
Analyze the transformed data to determine the correct data type for each column.
Examples of datatypes are: text, integer, timestamp, date.

Use the psycopg2 library to connect to the PostgreSQL database from your Python environment.
Install psycopg2 with pip: pip install psycopg2-binary
Use the provided credentials to establish the connection.

Iterate through the rows of your transformed Pandas DataFrame.
For each row, construct an INSERT INTO SQL statement.
Execute the SQL statement using the database connection.
Commit the changes to the database.
Finally push all code to your GitHub repository and submit the link
