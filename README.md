## NoSQL Database for SoundCloud's Music Streaming Data Analysis

This project involves designing and implementing a NoSQL database using Cassandra to efficiently query and analyze SoundCloud's music streaming data. The notebook details the process of modeling the data, executing queries, and validating the results to assist in understanding user behavior and song preferences.

### Project Overview:

1. **Introduction:**
   - **Objective:** The goal of this project is to create a NoSQL database for SoundCloud's music streaming data, which is currently stored in a CSV file. The database will enable efficient querying to analyze user activity and song preferences.
   - **Data Source:** The dataset contains information about songs and user activities on SoundCloud, originally stored in a CSV format.

2. **Cassandra Database Setup:**
   - **Cluster Creation:** The notebook begins by setting up a Cassandra cluster to connect to the database.
   - **Keyspace Creation:** A keyspace is created to define the scope of the data that will be stored and queried.

3. **Data Modeling:**
   - **Query 1:** 
     - **Objective:** Find the artist name, song title, and song length for a specific session and item in session.
     - **Data Model:** A table is created with a primary key composed of the session number and item in session to enable efficient querying.
     - **Query Execution:** Data is inserted and queried to validate the model.

   - **Query 2:** 
     - **Objective:** Retrieve the artist name, song title (sorted by item in session), and the user’s first and last name for a specific user and session.
     - **Data Model:** A composite key with user ID, session number, and item in session is used to allow sorted results.
     - **Query Execution:** The query is executed, and the results are validated.

   - **Query 3:** 
     - **Objective:** List the first and last names of all users who listened to a specific song.
     - **Data Model:** The primary key is designed to include the song title to facilitate this query.
     - **Query Execution:** The model is tested by inserting data and running the query.

4. **Database Cleanup:**
   - **Table Dropping:** All tables are dropped after the queries are validated to clean up the keyspace.
   - **Session and Cluster Closure:** The session and cluster connections are closed to ensure the resources are properly released.

### How to Use:

1. **Clone the Repository:**
   - Clone this repository to your local machine using `git clone`.
   
2. **Install Dependencies:**
   - Ensure you have Cassandra installed and running. Install any additional Python packages using `pip install -r requirements.txt`.

3. **Run the Notebook:**
   - Open the notebook in Jupyter and execute the cells in sequence to set up the database, model the data, and run the queries.

### Queries:

- **Query 1:** Find the artist, song title, and song length for a specific session and item.
- **Query 2:** Retrieve artist names, song titles, and user names for a specific user and session.
- **Query 3:** List users who listened to a specific song.

### Conclusion:

This project demonstrates the power of NoSQL databases like Cassandra in handling large-scale, unstructured data, such as music streaming records. By designing appropriate data models and queries, the project provides insights into user behavior and song popularity, enabling data-driven decisions for music streaming platforms like SoundCloud.
