# C195_Scheduling-App

### Purpose of the Application

### Author Information
Author : Alex Fair 

Contact Info : afair26@wgu.edu

application version: 1.0.1

date: 04/17/2023

### IDE and version number
IntelliJ IDEA 2022.3.3 (Community Edition)
Build #IC-223.8836.41, built on March 9, 2023,
Runtime version: 17.0.6+1-b653.34 amd64
VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o.


#### JavaJDK : Java 17.0.5
#### Javafx : openjfx-17.0.2
#### mysql connector: mysql-connector-j-8.0.32

### Program directions
*Must have the JavaJDK, javaFX and mysql connector versions above installed to run application. 

*Program requires a mysql database in order to run properly, connection details can be changed in JDBC.java in helper package.
Intelij CE by default should find the build file once it opens the parent directory of WGU-Scheduling-App.
However, if it does not automatically find when the directory is opened, if you go to the configurations of intelij
by hitting 'Alt+Shift+F10' and select edit configurations. Then in the top left corner there is a plus sign, click on that
and select 'Application'. then proceed to give it a name, select java 17 SDK and in the box next to it put
"scheduling_app.scheduling_app.Main". It should then run. But if you are missing the mysql-connector-j-8.0.32 
dependency. It is located at the top level in the folder called mysql-connector-j-8.0.32.


When the program launches the login screen is displayed. The user needs to enter a valid username and password (from the
mysql database) and hit login. Once they are logged in they are presented with 4 buttons; 
appointments, customers, reports and exit which will lead the user to their respected menus.

### Additional Report
For my additional report I displayed the busiest first level division by name with its number of appointments in a label and 
below that there is a table showing all the first level divisions with their number of appointments. I initially based it off
of the total appointments by month and by type but added in the first level divisions, so it was different. 
It goes through and iterates through each appointment finding the customerID, then based off the customer ID it goes and gets
that customers division name. If that current division name already exists in the division observablelist it adds 1 to the count.

It was more difficult than I had expected it to be until I found the comparator method to sort the list.
