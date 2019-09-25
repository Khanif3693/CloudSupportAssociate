DBA INTERVIEW.TXT

http://resources.infosecinstitute.com/ramp-5-levels-top-50-database-administrator-interview-questions/

Level 1: The Minion


What is a Database?
 a database is a collection of tables, structured in such a way that it can be navigated like you would any sort of table. If you remember in math class, you may have had a number of tables that allowed you to quickly find a value if you multiplied an x and y value together — or in this case, what it would be if you were looking for a particular row and column value.

Why should I go to all the trouble of creating a database when I have a perfectly good Excel Spreadsheet?

Scale. If you were to take a (singular) spreadsheet and a (singular) table and place them side by side, there would be effectively no difference in the data you are seeing or what you could do with it. As you go bigger and bigger with more and more tables and spreadsheets, if you have a black belt in spreadsheet-fu you can accomplish many of the same tasks that a database could do as well. The problem is, as you go larger and larger and larger, that it becomes much more difficult to be human-friendly and still be efficient when it comes to processing data. So should you replace every single spreadsheet with a database? Not necessarily, but if the data on that spreadsheet needs to be accessed quickly by multiple users simultaneously and is growing rapidly, it may be time to consider going to the dark side (they have cookies).

What is a query?

A query in normal terms is a question, simple enough. It is the statement that is talking to the database in order to Create, Read, Update or Delete (CRUD) data. While many times a query is an actual question asking for an answer, it can also be the statement to modify, insert, or remove data in the database as well.

What is SQL?

Structured Query Language is the basic way of asking a database server to talk to you. Whether that is in the context of asking it a question, giving it answers to questions it is asking you, or updating answers that have already been stored in the database. The art of asking the right question is critical to getting back the right data you need, which is incredibly valuable when dealing with databases, as it is very easy to receive far more data than you know what to do with, or nothing at all.

What does ‘SELECT’ do?

SELECT in the terms of an SQL query triggers a question to the database. It looks across the specified table(s), finds the data you are looking for and then presents it to the user for consideration. Depending on the query, this can be an awful lot of data, so again, asking the right question is critical.

What is a primary key?

A primary key is usually used as the index for a particular table — a value that the table can depend upon to be a reliable unique value in every row. When trying to pull data for a particular row, the primary key will normally be used to pull that information, usually a numeric value. For example, if you are trying to pull up data on a specific person, and that database is using their unencrypted ssn as the primary key (naughty), then that could be used in the query to identify that particular row since there could be other people present in the database with that specific name or other identifying characteristics.

What is a Database Management System?

A Database Management System, or DBMS, is essentially the application that handles the heavy lifting between you (the user), and the raw data. The database itself is just that — the database; it cannot alter its own data any more than the average person can re-arrange their genetic code. The DBMS is what you are talking to when you are asking the questions. It is what looks at your question, thinks about it for a while, goes to the database, picks up the data, hands it back to you, and asks you to come again.

What is the difference between a Navigational database and a Relational database?

The best way to describe a Navigational DBMS is through that of a tree. Each value was associated with another through the use of a parent, most of the time with no other direct way to access the data. Relational Databases on the other hand use values common to multiple tables to establish a unique key — making sure that they are talking on the same page so that there are many, many ways to get to the same place. To put it another way, if you were trying to get from point A to point B, a navigational database would have one specific path to get there — via a freeway. A relational database on the other hand would have options for taking the freeway, a back road, a boat, a plane, a bus and sometimes a rocket — provided that each of those methods were set up correctly to talk to each other. Most modern databases use the relational database model.

Why do most database types not talk to each other?

In a word: money. In three words: a lotttta money. Different database vendors spend a huge amount of research time trying to find ways to give them a leg up on the competition; whether that may be by performance, storage capacity, longevity, reliability, scalability, the list goes on and on. As a result, trying to be compatible and backwards engineer every single feature of a particular database type is difficult in the extreme before you even get to the patent violations. Most databases can be simplified down to filetypes like .csv files, which can be used to transport basic data from vendor to vendor. That being said however, there would be a lot lost in translation without help from higher up.

What is a Frontend?

For those that don’t want to see row upon row upon row of data in front of them until they go cross-eyed, a frontend is essential. In essence a management program, a frontend allows admins to be able to view and modify high level database functions without the need to use the command line for every single thing. This can be extremely useful not only for efficiency, but also for safety, as it can prevent accidental data modification. It can also allow users that are more used to a GUI application most of the utility that the CLI permits.



Level 2: The Researcher


What is a ‘join’?

Well when two tables love each other very much…not that much happens actually. However when you need to search across multiple tables simultaneously, a join can help make that happen. For example, if you were searching for information on a particular product and one table has the description while the other has pricing information, you can use a join to search across both tables simultaneously using a single query.

What is a foreign key?

When using a join or other type of query that goes across multiple tables, it can sometimes be difficult to make sure they are talking on the same page. A primary key can help with this, but sometimes this is impractical, and thus you need a secondary value that is consistent across multiple tables. For example, say that in a series of tables for product listings you have your primary key assigned to an auto-increment ID based on when the product was entered (a typical setup), and then none of these rows are able to line up with their counterparts in other tables. So if you have one table for product listings, another for price information, another for reviews, etc. — this could be a fairly major problem. However, if you know for a certainty that your part numbers for these products are going to be unique values, you can use that as a foreign key and suddenly everything lines up all nice and neat. This is possible since it exists in more than one table, and since is being referenced from outside its own table; it is designated ‘foreign’. This does not mean it still could not be the primary key for that particular table as well, it just means it has a reference that can be looked to from another point of view.

What is SQL Injection?

Also known as asking a question and getting the answer you want, rather than the answer they want to give you (anybody that has tried to navigate certain nameless support phones knows that this isn’t necessarily a bad thing); however in the context of a database application, this can be “a very bad thing”™. For instance, say that you are on an online banking website. You’re at the login screen, and it is waiting for you to enter your login and password so it can display your particular financial information. But what if you want to see the listing of everybody else that banks at this particular location? Depending on how the bank’s site is hardened against such an attack, you could get their personal information, current balances, PIN numbers, or even worse, enter your own data directly into the database — able to create new accounts, set up transaction history, active balances, the list goes on and on.

What is input sterilization?

One of the main answers to SQL Injection, input sterilization allows the database to selectively ignore data coming in from an input field and strip out non-required data. For example, if a field is expecting only a numeric value, there is no need for letters or symbols to be present in the user input. Therefore, these values can be safely ignored but still keep the functionality of the form intact. While not an end-all beat-all, it goes a long way to helping mitigate attacks on this vector.

SQL Vs NoSQL

NoSQL (Also called Not Only SQL), is a different form of database than the standard relational type. While it can use a lot of the same kinds of query language, it doesn’t necessarily use the same type of table structure that standard relational databases use, and thus in some cases can be more efficient. That efficiency depends greatly on its application however, and many times you will see NoSQL used in Big Data crunching and analysis applications that require real-time feedback.

What is ‘Big Data’?

DATA. If you’ve ever shopped on Amazon or at a Walmart, searched on Google or been on Facebook for more than 10 minutes, then you’ve seen Big Data in action. Big Data is essentially looking at the forest for the forest instead of the trees. An individual person is a unique entity with a specific set of actions and reasons for why they do what they do. Tracking an individual person’s actions can sometimes be useful, however it’s also a shot in the dark. But multiply that by many, many millions and suddenly the individual actions don’t matter as much — yet patterns start to emerge. A good example of this was published in the New York Times: Walmart discovered that just prior to a major storm, there was a run on the usual items such as bottled water, batteries and flashlights — but also strawberry pop tarts. This pattern was consistent across the board, so they were able to bundle these items together in certain parts of the store and increase profits. Amazon Suggestions, Google Analytics and other entities that run off of Big Data are huge moneymakers for their respective entities for being able to consistently give (relatively) accurate recommendations to users based on their past interests or purchases.

What is a ‘Flat File’?

A flatfile is a catch-all term used for concepts like Comma Separated Values (.csv). While there are a lot of different ways to create such a file, they all share ideas that they can be created and manipulated easily and without necessarily requiring a standard database application. These can also be used to transfer data from system to system due to their lightweight status. In some cases, these have been replaced by XML files, however XML can when compared to certain kinds of flatfiles, be very large.

I have a database that was built in MySQL, and I need the data to be moved over to Microsoft SQL Server. How would I do this?

The easy answer would be to contact Microsoft Tech Support and bring your checkbook. A more difficult answer would be to bring it down to a .csv file and then import it into SQL Server, but without a specialty conversion utility you may lose some program-specific specific tricks, thus requiring some rebuilding once the conversion is complete. This is not saying that this would work in all cases, but it is at least an option.

What is the difference between ‘=’ and ‘LIKE’?

When crafting a query, or using programming to display data in certain ways depending on the values being returned, you may want to think that these can be used interchangeably. There is one big difference, however: equal means equal. The value being returned must match the value it is being compared to 100%. LIKE, however, can be used with a number of different wildcard mechanics, allowing you to be a bit more flexible in your rules.

What is a Null Value?

A Null Value is an absence of data. This one is a bit misleading sometimes, because depending on who you ask, it can be considered many possible things. “Null equals 0”- Not in this context, because 0 is a value. “Null equals Empty” — closer, but again sometimes an empty value can still be considered a value depending on how the field is structured. If a column allows for null values, and no value is submitted, then it allows it to be Null.



Level 3: The Riddler


What does ‘INSERT’ do?

INSERT submits data into a database as a new row, usually through the use of a form. While forms can take many…forms…, the most common uses are through either a dedicated application or through the use of an HTML form. Clicking on the ‘submit’ button will trigger the built in form reaction to scan the form for particular fields, making sure the required ones are entered correctly, make sure the user isn’t being naughty in what they are trying to enter, then submit the data to the database.

What does ‘DROP’ do?

DROP removes a table from a database or a database from a server. A very dangerous command indeed, it is only to be used in situations that absolutely require it, as unless you have a backup of it handy, there is no coming back from this.

What is the difference between T-SQL and PL/SQL?

T-SQL or Transact-SQL is Microsoft’s version of SQL. The main additions Microsoft made to the main branch of SQL involve the addition of procedures or routines — scripts essentially — that can be run under certain criteria. PL/SQL, on the other hand, is Oracle’s version of SQL, and conceptually the two are very similar. However, because of the nature in how they were developed, trying to move data from one to the other involves quite a bit of work. The main differences deal with how they multi-task and how they lock elements when they are in use.

What does ‘UPDATE’ do?

UPDATE allows values to be modified where they meet specific criteria. For example, say that you were on Amazon and were about to move. As a result, you would want to adjust your mailing address so that you actually got your stuff. You would therefore go into your settings and it would show you your current address. Modifying this address and then submitting the form would update your address based on your particular user profile. If it updated anybody else’s address to match that would be a serious problem — at least for the person doing the paying.

Why do database servers benefit from a lot of memory, and why do 64-bit operating systems help in this regard?

Database servers like to cache as much data as possible when they are reading it a lot. Storing this information in active memory is a lot faster than trying to find it again from the hard disk or other media. Therefore more memory = faster response time = better performance. The problem is that for most operating systems the maximum amount of memory that can be used by a 32-bit OS is 4 gigabytes. While in years past this would have been an inconceivable number, today it is a drop in the bucket. 64-bit operating systems resolve this issue by being able to handle memory to 192 gigabytes currently for Windows, while Linux can theoretically go much higher at present, and these numbers will only climb higher and higher.

Why is it a bad idea to run a test on a live database?

On a test database, it’s relatively easy to keep the performance variables to a minimum. On a live database however, it needs to be functioning for all users all the time. Running untested code on a production database can not only reduce performance, but also create unforeseen instability in the server itself — potentially causing crashes and data corruption.

Why is it difficult to use standard file by file backup methods on an active database server?

This problem is twofold. First, many database servers place locks on database files that are currently in use. Most backup programs that try to do a file-by-file backup will therefore be unable to create a copy of this file, as they cannot get exclusive permissions to it. Second, while some database servers have only a single file to backup a database, others have multiple files that can be stored in different locations across possibly multiple physical hard disks. The problem can be resolved in one of two potential ways. First, using the backup method within the database server itself. Some programs such as Microsoft SQL Server allow you to create a scheduled backup directly within the server application to a location of your choosing. Others require you to use a scheduled task or another on-demand type of backup solution. The second would be to use a backup application that can talk directly to the database server, allowing the database to be backed up using a different technique.

When would you use an offline backup method versus an online backup?

If the above methods are unavailable when trying to create a backup solution, another potential method is temporarily taking down the database or database server in order to create a file-by-file backup. The problem with this method is that if the server goes down incorrectly, the backups could be flagged as bad and thus unusable. Periodically testing your backups to make sure they are working properly is strongly recommended, regardless of what method you use to create them.

What is Replication?

Database replication allows for real-time automated backups between multiple database servers. This allows for the creation of either a fall-over server, or warm backup for use in case the main server goes down.

Is data in databases encrypted by default?

While most database servers support some form of encryption out of the box, it is not enabled by default due to performance hits and security concerns.



Level 4: The Librarian


What is the difference between a ‘TINYINT’, an ‘INT’ and a ‘BIGINT’?

Contrary to popular belief, this is not the lifecycle of a talking tree. Rather, it is the creation of a column that allows for specific levels of integers (numeric whole numbers) up to a specified cap. There are many ways to limit the growth of fields, but in the case of Microsoft SQL Server, these each represent a value in bytes, which creates a maximum value that the field can hold.

Data type	Range	Storage
bigint	-2^63 (-9,223,372,036,854,775,808) to 2^63-1 (9,223,372,036,854,775,807)	8 Bytes
int	-2^31 (-2,147,483,648) to 2^31-1 (2,147,483,647)	4 Bytes
tinyint	0 to 255	1 Byte
How would you store files within a database?

Two common ways to store files for use by a database are either within the operating system’s file system, or within a field of the table itself. Uploading and storing the files outside of the database makes for faster creation of the application, and can be more efficient if the file sizes are larger, but can potentially cause security issues if the files are not secured correctly. On the other hand, the files can also be stored directly within the database using a BLOB-type field. A BLOB is a Binary Large Object, essentially an empty area where a file can be uploaded to but not exceed a specified limit. Like int in the example above, blob has a number of different potential sizes, depending on the type used. Bear in mind there are other methods for storing and accessing files in a database server, these two are merely the most common.

When would you use ‘char’ versus ‘varchar’?

This is a bit of a difficult question, mostly because it depends so much on what your application is. For example, if you have a form field that can be nearly any length and changes every single time, then varchar is a much more practical choice, since it gives you much more flexibility. If however you have a field where every value is going to be exactly the same length, then you can get more efficient performance out of a char. Again, it depends on exactly what your application is, and how you plan to cook it — seasoning as you see fit.

What is XML?

Extensible Markup Language (XML) is a fast way to display data that not only conforms to a structure that can be read by machines, but is also easily understandable by humans. Because they can be dynamically and manually generated in many different ways, they are easy to produce and map to; and because they retain the same structure despite the data being updated, they can be relied upon for automatic functions such as RSS aggregation.

What shows that a database server is running?

<Insert joke about needing to catch it here/> Database servers run as services or daemons, most times in the background without the necessity to see that they are running in order to interact with them. When things go sideways however, being able to verify that the service is in fact up and running can be an excellent place to start troubleshooting. Checking under the services area of your particular operating system, whether that be by GUI or by CLI, can show you that the service is started or not, thus allowing you either to start or restart it as need be.

What is WYSIWYG?

What You See Is What You Get. A mouthful of an acronym, it allows for the creation of an application that is consistent regardless of how it is viewed — whether on the design screen, being viewed in a browser or being printed. Creating an interface to a database that is not only functional but also looks nice is a trick in itself, and can take a lot of work to get it just right.

Why is it frowned upon to use ‘SELECT * ..’ in a large database?

Picture it like a group of people in line for a bathroom, and every single person that was going in there was going to use the toilet, change their clothes, take a shower, iron their jacket, take another shower, etc. There is only so much area that can be used efficiently before you start to get a queue, slowing down the whole operation that can eventually cause the entire thing to collapse under lack of toilet paper. You can quickly get back more than you can use or understand, so optimization is key when creating queries and asking only what you need to get the question answered.

How would you get the quantity of results from a query?

COUNT() is the main supported way to be able to get the number of returned results from a query. While there are many other options such as mysql_num_rows, these are considered obsolete and are being removed.

What is a Database Schema?

If you’ve ever seen one of those Visio diagrams with 40 different tables with lines connecting particular columns on one with those on another, that’s a database schema. Essentially a two-dimensional representation of how each table talks to other ones, it is the way to view the design of a database as a single entity and not as a jumble of different tables.

What are Nested Queries?

A query within a query, this particular method can be tremendously difficult to troubleshoot and even harder to manage without a lot of overhead. In most cases, a nested query can be replaced with a JOIN, allowing for much more efficient use of resources.



Level 5: The Caretaker

What is ODBC?

Open Database Connectivity is a way to make different kinds of frontends talk to different data sources (DSNs) such as Databases. The specifics available depend on the type of application being used, the driver being used and the backend to which it is being applied.

For Oracle systems, what is OFA?

Optimal Flexible Architecture (OFA) is the recommended layout for installing and configuring an Oracle database.

For Oracle systems, what is error “ORA-01034”?

The full error is “ORA-01034: ORACLE not available”. While there are many potential causes, the most common is that the service is just not running. The resolution is to start the service, then see if the error comes back.

What is Normalization?

When most people first start working with databases, the first instinct is to create massive tables for storing data — one place, one query — keeps things simple. However, as they grow to unmanageable levels, it is a good idea to look into Database Normalization. This idea allows for data to be split off into smaller more efficient tables that (hopefully) reduce the amount of duplicate data. In this way, smaller queries can be run on individual tables instead of having everybody always talking to one big one — thus improving performance.

For Microsoft SQL Server, what is a DMV?

Dynamic Management Views are functions built into Microsoft SQL Server that allow for troubleshooting, diagnostics and server health monitoring.

What are the default ports for MySQL, SQL Server and Oracle, and can/should this be changed?

The default port for MySQL is 3306, and can be changed in Windows as noted in this article or in *nix as noted in this article. The default port for Microsoft SQL Server is 1433, and can be changed as noted in this article. The default port for Oracle is 1521, and can be changed as noted in this article. Depending on your security stance, changing the port that your database server uses can be a good way to lower your profile and reduce the amount of unauthorized access attempts against the server.

For Microsoft SQL Server, What is Log Shipping?

A form of backup on Microsoft SQL Server, Log Shipping is similar to replication and allows for rapid failover if the main server goes down. One thing to bear in mind, however, is that a log shipping based failover must be activated manually; it will not switch over automatically.

For Microsoft SQL Server, what is DBCC?

Database Console Commands (DBCC) are a series of utilities for SQL Server designed for maintenance and reporting. A full list of the commands can be found here.

What is Cloud Computing?

Cloud Computing is usually a catch all term for data being stored “over there”. Placing high-requirement applications onto dedicated hosting services can be beneficial depending on the application, however it can also cause catastrophic security problems and availability issues. It is therefore highly recommended to keep important data in-house, and only outsource in situations that it cannot be avoided. Cloud Computing, Big Data and Data Mining are many times talked about in the same sentence since processing power required for one usually means the others become viable either as a requirement or a side effect.

What is Hadoop?

Hadoop is a Data Mining application designed to handle very, very large amounts of data across a wide variety of environments — from one to thousands of systems. Used in situations that don’t necessarily fit into standard database structures, its main strength is being able to take one giant project and split it off to each of its member servers, have them each process their own job, then have their findings recombined into one viewable result.
