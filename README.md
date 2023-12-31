# Concert Ticket Reservation System

### Introduction:
The Concert Ticket Reservation System was designed to help users book tickets to local concerts. The key objectives of this system are to manage ticket sales, concert information, user reviews, promotion schedules, and staff management. Inspired by connecting audiences with local artists, the project allows users to centralize their concert experience by enabling finding concerts, buying tickets, and sharing experiences through reviews using a graphical user interface (GUI), tkinter.
Additional to a user view, the system also enables staff to centralize their management practices using an admin view. The overarching goal of this system was to improve the general concert experience for both users and staff.

### Database design:
![Project Final ERD](https://github.com/pranavneu/concert_system/assets/154646829/5b0ec0b3-fda1-4ef4-8fc4-b41ba0d8afa7)

### Data Collection
This databases’s data was primarily generated by python’s Faker library. The Faker library generates fake data effectively for a great variety of fields for when realistic but not real data is needed. Additonal libraries used were pymysql, datetime, cryptography, and random. The general procedure of data generation was similar for all tables. The first step was to use pymysql to connect to the MySQL server.
After the connection and cursor have been established, and creating a loop iterating over the primary key, fake data was generated for each primary key in the iteration. While still in the loop, each iteration of fake data was inserted into MySQL using the cursor. Outside the loop, there is a print statement for each newly inserted row of the table to verify the data. Once the proper insertion of data
has been verified the changes are committed to the MySQL server and the cursor and connection are closed.
There are several key differences that can be observed across the different data insertion functions. When looking at attributes with values that may be repeated, such as genres in the songs table, a list of values was made by hand. This was done due to how some attributes needed fixed values to be repeated at random across multiple rows in each table.
In addition to this, the foreign keys in each table also needed to manually be inserted into each table. This was done due to a technical limitation of the faker library, where, when trying to create fake foreign keys, the foreign key values would be skipped during some iterations, leaving null values in their place. When trying to solve this, one solution would have been to run the loop multiple times to give the program the chance to fill in the missing values. This solution, however, did not prove to be reliable. This conclusion was made with the understanding that there was no guarantee the null values would be filled in after running the program any number of times.
Since the data was generated at our discretion, there was no need for specific cleaning or preprocessing as the data was manually checked and created at each iteration.

### Application Description
The graphical user interface (GUI) within the application has been made using the Tkinter library, a robust Python framework dedicated to facilitating GUI development.

**Libraries Used**
1. tkinter
2. MySqlConnector
3. datetime
4. random

### Conclusion
Conclusion/Future Directions
This project allowed for a deeper understanding of database design techniques through effective implementation. The various tasks such as data normalization in 3NF, implementation of the Faker Library in python, using mysql-connector to connect Python to the database, and working with triggers, stored procedures, views, and more all helped solidify the usefulness of MySQL. In terms of future directions, there are various ways to expand and improve this project. One simpler way could be to connect the reviews and concert table using a foreign key. In this case, user reviews could be connected to a specific concert. As the project stands now, users are unable to see the specific concerts each review references and instead see a general review of all concerts available. This functionality would improve the user experience and allow them to make better decisions when purchasing tickets. This would also be needed due to how the opinion on one concert may be different from others.

### Installation steps
1. **Download the database dump file:**
   - Download the music_reservation_dump.sql file.
2. **Database Setup:**
   - Import the  music_reservation_dump.sql file into your database.
   - This file contains both the Data Definition Language (DDL) for table creation and the Data Manipulaiton Language (DML) for data insertion.
3. **Update Data (Optional):**
   - If updates are needed, use the project_INSERT.py python source file.
   - This file with the help of the faker library has been used to generate the data.
4. **Frontend Setup:**
   - Donwload the project_SOURCE_CODE file for the frontend.
   -  Ensure that all libraries mentioned in the application description are installed.
5. **Configuration:**
   - In the project_SOURCE_CODE file, locate and replace the placeholders for 'user', 'password', and 'database' within the approprite functions. Ensure that these fields correspond to your MySQL server credentials.
6. **Running the application:**
   - Once everything is done, execute the project_SOURCE_CODE file.
   - The Tkinter window will appear, connected to the backend server.
7. **Troubleshooting:**
   - If you encounter any issues during installation, feel free to reach out for assitance at pranavkantha@gmail.com

### Contributors:
[Pranav Kanth Anbarasan](https://www.linkedin.com/in/pranav-kanth-anbarasan-b5b93818a/)  
Hasan Khwaja  
Sreeja Vepa  





