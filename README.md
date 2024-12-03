# Gemini SQL Query Retriever

## Aim

The aim of this project is to develop an AI-powered application that converts natural language questions into SQL queries, retrieves the corresponding data from an SQLite database, and presents it to the user. The application uses the Google Gemini 1.5 model to process user input and generate SQL queries for querying a pre-existing database. The system helps users efficiently retrieve data by simply asking questions in natural language, making it more accessible for non-technical users.

## Methodology

The methodology behind this system involves the following key components:

1. **Natural Language Processing**: Google Gemini 1.5 is used to process natural language input (user questions) and generate corresponding SQL queries.
2. **SQLite Database**: The application uses an SQLite database (`student.db`) to store and retrieve student data.
3. **Streamlit Interface**: A Streamlit web interface allows users to input questions, submit them, and view the results of the generated SQL queries.
4. **SQL Query Generation**: The user inputs a question (e.g., "How many students are in the Data Science class?"), which is processed by the Gemini model to generate an SQL query.
5. **Database Query Execution**: The generated SQL query is executed against the SQLite database to retrieve the required data.
6. **Results Display**: The results of the database query are displayed to the user via the Streamlit interface.

## Evaluation Metric

The system's effectiveness can be evaluated based on the following criteria:
1. **Accuracy of SQL Query Generation**: The system’s ability to generate the correct SQL query based on the input question.
2. **Correctness of Database Query Execution**: The system should return accurate results based on the query execution against the SQLite database.
3. **User Experience**: The simplicity and intuitiveness of the user interface and the ease of retrieving data.

## Results

The system allows users to input questions in plain English, and it generates accurate SQL queries that are executed against the `student.db` SQLite database. For example, the following question:

**Input:** "How many students are in the Data Science class?"

Results in the generated SQL query:

```sql
SELECT COUNT(*) FROM STUDENT WHERE CLASS="Data Science";
```
The system then executes the query on the database and displays the results:

**Output:**

The number of students in the Data Science class.

## Conclusion
This project demonstrates an effective use of AI in simplifying the process of querying databases. By using the Google Gemini 1.5 model, the system can convert natural language questions into SQL queries, making it accessible to a broader audience, including those without technical knowledge. The integration of the SQLite database ensures that the system is efficient and can handle real-time data retrieval. The user-friendly Streamlit interface further enhances the user experience.

## Future Work

**Support for Complex Queries:** Extending the model to handle more complex queries involving multiple tables and join operations.

**Multilingual Support:** Adding support for queries in multiple languages to make the system accessible to a global audience.

**Database Expansion:** Integrating with larger, more complex databases to test the scalability of the system.

**Advanced Query Optimization:** Implementing mechanisms to optimize generated SQL queries for better performance.

**Integration with Other Databases:** Expanding the application to support other database types like MySQL, PostgreSQL, etc.

## How to Run

**Prerequisites:**
Python 3.x
Google Gemini API key (add this to a ```.env``` file)
SQLite3
Required Python packages from ```requirements.txt```

**Installation** 

1. Clone the repository:
```
git clone https://github.com/username/Gemini-SQL-Query-Retriever.git
cd Gemini-SQL-Query-Retriever
```
2. Install the dependencies:
```
pip install -r requirements.txt
```
3. Set up the Google Gemini API key in a ```.env``` file:
```
GOOGLE_API_KEY=your_google_gemini_api_key
```
4. Set up the SQLite database (```student.db```) by running the ```sqlite.py``` script to create the database and insert sample data:
```
python sqlite.py
```
5. Run the Streamlit application:
```
streamlit run app.py
```
6. Open the provided local URL in your browser to use the app.

License
This project is licensed under the MIT License.



















