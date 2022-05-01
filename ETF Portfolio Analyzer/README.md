# ETF Portfolio Analyzer

In recent years, finance has had an explosion in passive investing. Passive investing <br> means that you invest in a basket of assets that’s called an exchange-traded fund (ETF). <br> This way, you don’t spend time researching individual stocks or companies or <br> take the risk of investing in a single stock. We present to you a Portfolio Analyzer that utilizes <br> a financial database along with Python, Pandas, Voila, and SQL.

This service includes:
1. Analysis of a single ETF
2. Data access optimization with advanced SQL queries
3. Analysis of the entire ETF portfolio
4. Deploying the Notebook as a Web application via Voila

---

## Technologies

This service utilizes Python 3 and the following libraries:
1. Pandas
2. SQLalchemy
3. Voila

---

## User Guide

To begin using the notebook in Jupyter Labs:

### Part 1
1. Open "etf_analyzer.ipynb"
2. Look for the following:
    ```python
    database_connection_string = 'sqlite:///etf.db'
    engine = sql.create_engine(database_connection_string)
    engine.table_names()
    ```
Please ensure that you have the correct .db file imported from the parent folder.
3. Run each code cell to retrieve your data.

### Part 2
1. Look for the following:
    ```python
    query = """
    SELECT time, close
    FROM PYPL
    WHERE close > 200.0
    """
    ```
This SQL query is vital towards extracting the data used in further cells.

### Part 3
1. Look for the following:
    ```python
    query = """
    SELECT *
    FROM GDOT 
    INNER JOIN PYPL ON GDOT.time = PYPL.time
    INNER JOIN GS ON PYPL.time = GS.time
    INNER JOIN SQ ON GS.time = SQ.time;
    """
    ```
After inputting the relevant table names, please ensure your syntax follows the above code. Absence of the correct SQL syntax <br> could result in a mis-join of tables or inability to extract data.

---

## Documentation
Please reference the following screenshots for guidance with any changes within the code:

SQL Connection                        |  Demo Connection
:------------------------------------:|:------------------------:
![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/SQL_Connection.PNG)                      |  ![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Demo_Connection.PNG)

Query                                 |  Demo Query
:------------------------------------:|:------------------------:
![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Query.PNG)                      |  ![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Demo_Query.PNG)

Voila 1                               |  Voila 2
:------------------------------------:|:------------------------:
![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Voila_1.PNG)                      |  ![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Voila_2.PNG)

Voila 3                               |  Voila 4
:------------------------------------:|:------------------------:
![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Voila_3.PNG)                      |  ![Alt text](https://github.com/antonmaliksi/FinTechModule7Challenge/blob/main/ETF%20Portfolio%20Analyzer/Readme%20Resources/Voila_4.PNG)

---

## Contributors
Coding was completed by Anton Maliksi with colaboration from Colton Mayes, James Handral, Aarchit Malhotra, Babin Stresha, and Lucas Manning.

---

## License
No licenses were used for this application.
