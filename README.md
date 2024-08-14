
# SQL Database Question Answering with RAG and LLM

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) application for answering questions using a SQL database and a language model (LLM). The project connects to a SQLite database, generates SQL queries based on user input, and returns answers augmented by the LLM.

## Project Structure

- **Notebook**: The main logic is contained in the Jupyter notebook `rag_sql_database_question_answer.ipynb`.
- **Database**: A sample SQLite database `street_tree_db.sqlite` is used.
- **LLM**: The project uses the Groq language model via the `langchain_groq` package.

## Prerequisites

- Python 3.8 or higher
- Virtualenv
- Jupyter Notebook

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. **Create a Virtual Environment**

   Create a virtual environment to isolate the project dependencies.

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies**

   Install the required Python packages.

   ```bash
   pip install -r requirements.txt
   ```

   If a `requirements.txt` file is not provided, you can manually install the necessary packages:

   ```bash
   pip install langchain_groq langchain_community langchain_core python-dotenv
   ```

4. **Set Up Environment Variables**

   Create a `.env` file in the project root with the following content:

   ```bash
   GROQ_API_KEY=your_api_key_here
   ```

   Replace `your_api_key_here` with your actual Groq API key.

5. **Run the Jupyter Notebook**

   Launch Jupyter Notebook to run the project:

   ```bash
   jupyter notebook
   ```

   Open the `rag_sql_database_question_answer.ipynb` file and run the cells to execute the project.

## Usage

- **Querying the Database**: Input your questions in the notebook, and the system will generate SQL queries, execute them on the database, and return an augmented answer.
- **Customizing the LLM**: You can modify the LLM parameters in the notebook, such as `temperature`, `max_tokens`, etc., to adjust the output according to your needs.

## Notes

- Ensure that the SQLite database file `street_tree_db.sqlite` is present in the `data/` directory.
- This project is a basic use case and can be expanded for more complex applications.
