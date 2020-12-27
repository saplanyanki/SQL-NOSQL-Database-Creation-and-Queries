# SQL-NOSQL-Database-Creation-and-Queries
Introduction
1) The dataset that we chose was the firearm permits and background checks database. The data analyzes the United States, state by state and we thought it would be a good choice for this project as we have a dataset that has many options to work with.

Firearm permits and background checks Dataset
Dataset: https://github.com/BuzzFeedNews/nics-firearm-background-checks

We used the firearm permits and background checks data. The data goes by each state, and the month for that state. The data has over 20 years of data, 12 months for
each year, and then every state and American territory. The data has some huge discrepancies, both over time and between states. You can see the certain laws or
requirements from each state and that time period by looking at the numbers. Overall, the data is very good for analyzing firearm permits and background checking over the past 20 years and for each state. The data appears to have come from Buzzfeed and I think the only limitation in the dataset is that it doesn’t account per capita. The numbers can be slightly misleading due to population size differences, but it does very well with showing possible laws or the political environment of a time period and state.

2) The data in this repository comes from the FBI’s National Instant Criminal Background Check System. The NICS is used by the Federal Firearms Licensees to instantly determine whether a prospective buyer is eligible to buy firearms or explosives. Before ringing up the sale,
cashiers call in a check to the FBI or to other designated agencies to ensure that each customer does not have a criminal record or isn’t otherwise ineligible to make a purchase. There have been more than 100 million checks over the past decade, which has led to more than 700,000 denials over that timespan. The code in this GitHub repository downloads that PDF, parses it, and produces a spreadsheet/CSV of the data. The data collects data from about the last 20 years, ranging from November 1998 to April 2019.

The dataset we are working with contains these attributes:
● month
● state
● permit
● permit_recheck
● handgun
● long_gun
● other
● multiple
● admin
● prepawn_handgun
● prepawn_long_gun
● prepawn_other
● redemption_handgun
● redemption_long_gun
● redeption_other
● returned_handgun
● returned_long_gun
● returned_other
● rentals_handgun
● rentals_long_gun
● private_sale_handgun
● private_sale_long_gun
● private_sale_other
● return_to_seller_handgun
● return_to_seller_handgun
● return_to_seller_long_gun
● return_to_seller_other_totals

# Introduction or background
The firearms data basically shows a lot of different firearm statistics according to their state and their month/year. The data shows how many individual totals(firearms) and other neat statistics, including permits and permit rechecks. I think that the data is interesting because you’re able to see the difference in laws between states. The huge discrepancy in some of the data shows what is required with firearms in some states, and possibly the politics surrounding firearms in each state and their time period.

# Installation
First, I downloaded the required files and data including the csv data from the github repositories. After downloading the DB Browser for SQLite, I have imported the csv data into a new database table. The first row had a problem while executing the sql command as the database table inserted the columns as rows. After fixing the mistake SQL execution was working, and I was able to run SQL commands we have decided on.

# NoSQL (MONGODB)
Importing to the MongoDB terminal.
For MAC users:
1) cd to desktop where file is located
run on terminal: mongoimport -d mydb(give a name) -c things(table name) --type csv(or json) --file nicsfirearm.csv --headerline(cant do on json)
2) you should have imported 14465 documents succesfully under selected database under MONGODB
3) %brew services list (shows you if mongodb running successfully)
4) use mydb <--- run this on terminal to switch databases
5) db.things.find() <--- run to see all your data if wanted to pretty()

# Conclusion
I was able to pull out the same output, although I have received a lot of errors at first.
Firstly, loading the csv data into my database took some time, even though I reloaded it
for 30 minutes. After I solved that problem, there was a problem when I executed my
commands, first one was that sql did not understand ‘state’ and ‘month’ as a column,
instead executed as an inbuilt function which made me change the column names to
‘states’ and ‘months’. Another error that took me so long to understand was that IST

# Discussion
First, both of us both agreed that we like using the DB Browser for SQLite because it felt
a lot cleaner and less clunky than other database methods used in the past. This
program was very easily navigable and simple to upload our data into. It was also a lot
faster and smoother, I would assume because we aren’t “logged into” a PSU computer.
I think for circumstances involving the organization of data, the DB Browser would be
better due to a simple infrastructure and easy usage once the data is imported.
The obvious differences between the NoSQL tool and the relational tool is the look and
how the data is interpreted. I’d argue that the relational tool has a very clean cut look to
it that helps look at the data. The SQL tool also had many buttons, or different methods
of using the program, it was much simpler to use. The SQL section of the project took a
much shorter duration than its NoSQL counterpart. The NoSQL data tool was all coding
and a lot less user friendly. Taking a lot more time with this tool and its less-inviting
infrastructure sums up the time using MongoDB SQL accepts single quotes where my SQLite accepts double quotes. 
