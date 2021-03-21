##Roles and skills of data professionals
###Data analytics
* Output is used internally to make business decisions
* Analyse data for the purpose of making a decision/ answer questions
* For example:
  * What happened?
  * Why did it happen (root causing)?
  * What is likely to happen (forecasting)?
  * What action should we take?
* Background: Open ended
* Skills: SQL/ Communication/ Biz Acumen
* Roles: Analyst/ Marketing/ BI

###Data science
* Output reaches external customers
* Decision based (advanced statistical modelling) * complex solutions on what action should we take
* Feature*based (building data products)* shopping recommendations, advertisement targeting, netflix tv suggestions
* Background: CompSci, Quantitative Field (Physics, Math, Statistics)* Graduate degree!
* Skills: Programming (Python & R)/ Statistics
* Roles: Data Scientist/ ML Engineer

### Data engineering/ data infrastructure/ data architecture
* Collection, storage, processing and transfer of data that enables data analytics and data science
* eg implementing infrastructure allowing real*time recommendations to display immediately after activity on the site
* Background: CompSci/ Software Engineering
* Skills: Programming/ Database system
* Roles: Data warehousing, developing and maintaining distributed systems, and building data pipelines

## The data analytics "tool triangle" </h2>
1. Spreadsheet
2. Database & SQL  (we store data in a database, we access the data in our database by writing SQL, we write SQL in a SQL client)
3.BI Software

##Data pipeline: how data moves from collection to analysis</h2>
Data source > raw data > raw data database > ETL > Analytic database > Analysis
External data source > raw data > API> ETL >^

###ETL
1. Extract: Pull raw data out from a database
2. Transform: Do stuff to the raw data (convert, delete, filter)
3. Load: Store transformed data in to a separate database (this database is called the analytic database)

###API Application Programming Interface
Technology that bridges systems together and enables the sharing of data
