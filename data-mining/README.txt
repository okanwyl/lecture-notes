## Start of CHAPTER 1
# What is data mining?

- Simply stated, data mining refers to extracting or "mining" knowledge from large amounts of data (sand gold relation)
- Knowledge Discovery From Data, KDD synonym for data mining 
- Knowledge discovery process iterative sequence
1. Data Cleaning ( to remove noise and inconsistent data)
2. Data Integration (where multiple data sources may be combined)
3. Data selection (where data relevant to the analysis task are retrieved from database)
4. Data transformation (where data are transformed or consolidated into forms appropriate for mining by performing summary or aggregation operations, for instance)
5. Data Mining (an essential process where intelligent methods are applied in order to extract data patterns)
6. Pattern evaluation (identify truly interesting patterns)
7. Knowledge presentation (visualize)

- 1 to 4 is different forms of data preprocessing
- Standart architecture of typical data mining system consist components are
1. database
2. data warehouse
3. world wide web
4. other info repos
5. database
6. data mining engine
7. pattern evaluation
8. user interface
9. knowledege base

# Data Warehouses (work on that?) @TODO
-OLAP qubic (drill up drill down @TODO)
ex: 
-> vancouver, attributes address:toronto, new york, chigaco (top face)
-> front face attributes time(quarter): q1,q2,q3,q4

# Transactional Databases
- each transaction added to the database


# Object-relational Databases
- object oriented wrapper you know that

# Temporal Databases, Sequence Databases, and Time-Series Databases
- Temporal database stores relational data that include time-releated attributes
- Sequence Database stores sequence of ordered events
- Time-series Databases stores sequences of values or events obtained over repeated measurements of time(hours,daily,weekly)


# Spatial Databases and Spatiotemperal Databases
- Spatial database contain spatial(uzamsal)-related information such as maps geography
- Spatial data may be presented as a raster format(just a image format like png jpg but in a matrix)
- Spatiotemperal databases are same but changes in time

# Text databases and Multimedia Databases
- Text Databases are stores Long sequence of words.
- Multimedia databases you know that 

# Heterogeneous Databases and Legacy Databases
- Heterogeneous database consists a  set of interconnected, autonommous component databases.
- That's legacy?

# Data Streams
- Where data flow in and out of an observation platform or window dynamically.
- Huge or possibly infinite volume, dynamically changing, flowing in and out in a fixed order
- Often real time
-   

# Data Mining Functionalities
- Data mining tasks can be classified into two catagorioes : descriptive, predictive


# Concept/Class Description : Characterization and Discrimination

- Data characterization is a summarization of the general charecteristics or features of a target class of data.
Ex: To study the characteristics of a software products whose sales increased by a %10 in the last year, data can be
collected by SQL query

# Mining frequent patterns, Associations and Correlations
- Frequent patterns General assumption ex: PC vendor that customers buy frequently appear together in a transactional data set
PC -> digital camera -> memory card is a frequent sequential pattern

- Association analysis: 
Ex: Electronics transactional database
buys(X, "computer") => buys(X, "software") [support=1%, confidence=50%]
where x representing customer 
confidence meaning: %50 means that if customer buys a computer there is a chance of %50 that she will buy software
as well.
support meaning: %1 of all of the transactions under analysis showed that computer and software purchased together
that was single demansional if we use ^ icon on the left query that becomes multidimensional association rule


# Classifaciton and Prediction
- Decision trees, neural network, regression analysis 
Ex: IF-THEN rules
age(X, "youth") AND income(X ,"high") => class(X, "A")
age(X, "youth") AND income(X ,"low") => class(X, "B")
age(X, "middle_aged") => class(X, "C")
age(X, "senior") => class(X, "C")

# Cluster anaylsis
- Unlike classification and prediction which analyze class-labeled data objects, clustering analyzes data objects
without consulting known a class label.

# Outlier analysis
- A database may contain data objects that do not comply with general behaviour or model of the data.
- Most data mining methods discard outliers as noise or expections
- Rare case events can be more intersting than the more regularly occuring ones referred that as a outlier mining
Ex: fraud detection

# Evolution analysis
- models regularities or trends for objects whose behavior changes over time.
Ex: major stock market(time-series)


# Classification of Data Mining Systems @TODO

# Integration of a Data Mining System witha Database or Data Warehouse System
- No coupling: DM(Data-mining) system will not utilize any function of a DB or DW system.
- Loose coupling: DM(Data-mining) system will utilize function of a DB or DW system.
- Semitight coupling: Semitight coupling means that besides linking a DM system to
a DB/DW system, efficient implementations of a few essential data mining primitives 
(identified by the analysis of frequently encountered data mining functions) 
can be provided in the DB/DW system. These primitives can include sorting, 
indexing, aggregation, histogram analysis, multiway join, 
and precomputation of some essential statistical measures, 
such as sum, count, max, min, standard deviation, and
so on.
- Tight coupling : smoothly integrated


# Integration of a Data Mining System witha Database or Data Warehouse System




## End of CHAPTER 1


## Start of CHAPTER 2 text book 3

Data: raw, atomic, mostly operational
Information: processed, re-organized, grouped
Knowledge: patterns, models, findings 'behind' information
Wisdom: perfect orchestration of knowledge

Data warehouse is subject-oriented, integrated, time-variant and nonvolatile collection of data

Subject-oriented: major subjects -> customer supplier product and sales
Integrated: constructed by integrating multiple heterogeneous sources
time-variant: element of time provide information from a historical perspective
Nonvolatile: data warehouse doesn't contain data transformer applications

## End of CHAPTER 2 text book 3

