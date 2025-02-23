# Natural-Language-Schema-Filter
A Python-based solution that converts natural language queries into SQL statements. It processes user queries, extracts keywords, filters relevant database tables, and generates structured SQL queries dynamically.


# Natural Language to SQL Query Processor

This project processes natural language queries and converts them into SQL queries based on a given database schema. It allows users to extract relevant information from a structured database using simple English queries.

## Project Structure

├── data/
│   ├── schema.json       # JSON representation of the database schema
│   ├── schema.yaml       # YAML representation of the database schema
│
├── database/
│   ├── ecommerce.db      # SQLite database file
│
├── src/
│   ├── main.py           # Main entry point to run the query processor
│   ├── output_formatter.py  # Formats the query results for display
│   ├── query_processor.py   # Extracts keywords and generates SQL queries
│   ├── schema_filter.py     # Filters relevant tables based on extracted keywords
│   ├── schema_loader.py     # Loads database schema from JSON/YAML files
│
├── tests/
│   ├── test_query_processor.py  # Unit tests for query processing


## Features
- Converts natural language queries to SQL
- Extracts relevant keywords from queries
- Filters necessary tables and columns dynamically
- Supports SQLite database schema loading from JSON/YAML
- Provides formatted query results
- Includes unit tests for validation

## Installation
### Prerequisites
- Python 3.8+
- SQLite3
- Required Python packages from `requirements.txt`

### Setup
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure `ecommerce.db` exists in `database/`.

## How to Run the Code
### Running the Query Processor
To execute a natural language query and generate SQL:
```bash
python -m src.main data/schema.json "Show me all orders with customer names and order totals from the last month."
```

### Running as an API (Using FastAPI)
1. Start the FastAPI server:
   ```bash
   uvicorn src.main:app --reload
   ```
2. Open your browser and visit [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) to interact with the API.

### Running Tests
To validate the functionality, run:
```bash
pytest tests/
```

## Future Improvements
- Expand database support beyond SQLite
- Improve NLP query parsing accuracy
- Add support for advanced SQL queries (e.g., joins, aggregations)

## License
This project is licensed under the MIT License.

