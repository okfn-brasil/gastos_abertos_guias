# 1. CSV -> JSON Schema describing the data

 A program that will infer the data types from a CSV files and try
 to find relations/hierarchy between the columns. First this
 program will have a command language interpreter (CLI), but later we will develop a web frontend
 for it.

   * Datetime columns
   * Categorical columns
   * Hierarquical relation between columns.

 **Input:** CSV File

 **Output:** JSON Schema describing de model (JSON data source)

# 2. JSON Schema -> JSON Schema describing the Database Model

 The database model could be a relational database, NoSQL or simple
 a flatfile. The reason of this JSON Schema describing the model is
 for the use of another program for the creation of the model in
 some backend.

**Input:** JSON Schema from 1

**Output:** JSON describing the model (JSON data model)

# 3. JSON Schema for the Model -> RESTful API

Program that create an API with endpoints from JSON data model and data source
endpoints for data export or async requests.

**Input:** JSON Schema from 2

**Output:** Run a RESTful API

# 4. Data validation when importing data for the model created at 2
