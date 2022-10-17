# Store-Data-Python-SQLite

This is a good Python/SQLITE project which gave a good experience of using Python for Data Cleaning and Python's 'SQLITE' module to perform SQL queries

I thank my university Birkbeck, University of London for this project. The Codes are my own

1. You have been given sales and advertising spend details for 90 of their
stores in 6 cities, namely London, Birmingham, Cardiff, Manchester,
Bristol and Glasgow.

If a store area is less than 1000m2 then its store size is defined to be
small, if it greater than 4000m2 then its store size is defined to be large,
else its store size is defined to be medium.

The data is held in two csv files :

i. A list of the total value of all annual sales per store for the ten
years 2010-2019, plus some other details about the store (so 90
“records”)

ii. A list of the total (planned) marketing-spend per store for each
pair of years during the same period, i.e., 2010-2011, 2012-2013
etc. (so 45 “records”)

Your boss requires you to store the data in a database then produce
some simple statistics graphs on the data as follows.

(a) Plan and the create a normalised SQLite database from these two
files. Your database should contain at least three tables

(b) Create a new field in one of your tables that reflects the store size
of the store as defined above. Populate this field with the correct
data

(c) Produce the minimum, mean and maximum yearly sales for each
of the three store sizes for each of the ten sales years

(d) Plot the means for one of the three store sizes over each of the
ten years using an appropriate graph with all three sets of the
same graph

Use Python and its SQLite module for the database work, and an
appropriate Python graphing module (use matplotlib or similar) for the
graphing in part (c).

2. The sales spend for the other stores is held in a different format,
namely each year’s sales are held by quarters in a single JSON file.

Your boss now requires you to be able to read the data from the given
JSON file, categorise the store size as small, medium or large, and then
note how its sales compared to the stores of its size in Question 1.

Specifically, you must write a Python function that reads the given JSON
file and returns a dictionary containing the following information:

i Name of store, city, postcode and when opened

ii Store area and store size (i.e., small, medium or large as in
Question 1)

iii Year and total yearly sales for this year

Ensure you actually run the program to check it returns the correct
results. Then make some brief observations in your write-up how this
store’s sales for this year compares to the other stores of the same size
from Question 1.


3. Finally, your boss wants to look at changing future marketing spend. They ask you to take the ten stores of small size with the lowest sales in
the last two years of data you have, namely 2018-2019, and the corresponding marketing spend. They then want you to make thefollowing (admittedly wild) assumptions

i. The ratio of marketing spend to sales remains constant when you increase or decrease the marketing spend, i.e.,
  o if you spend twice as much, you double the sales
  
  o if you spend half as much, you half the total sales
  
  o if you do nothing, the sales do not change
  
ii. The total marketing-spend for 2020-2021 for these ten stores
must be the same as the total marketing-spend for 2018-2019

iii The marketing-spend for a single store cannot be less than half or
greater than double of its 2019-2019 spend
With these three assumptions, your boss wants to know how to
distribute the 2020-2021 marketing spend for these ten stores in order
to get the greatest total sales from these ten stores over those two
years?

Specifically, you must

(a) Use Python and SQLite to

i. identify the ten stores in the small size category with the
lowest total sales for the period 2018-2019 (i.e., the sum of
both years per store) and return their sales

ii. obtain the marketing spend for each of these ten stores
and thence obtain the total marketing spend for these
stores for the period 2018-2019

(b) Plan and then write an algorithm in Python to work out how
much to give each store to spend on their marketing in 2020-
2021 so that the total sales of the ten stores is maximised over
the same period. Please return the total marketing spend per
store, the expected sales per store and thence the total expected
sales

