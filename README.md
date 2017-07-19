# info-handling-cassandra-app
Info-handling-cassandra-app() Product: a single page web application with REST for information handling. Student information created using cassandra db and maven as a project directory. The following tools and frameworks are applied to develop the app. 


Single Page Web Application with REST for Student information handling.

Pre-requisites:
                         - Maven 3.x
                         - Java 1.7 or above
                         - JBoss AS 7

Used Technologies/Frameworks:

                         - HTML
                         -CSS
                         -Spring
                         - Cassandra
                         - AngularJS 
                         - Bootstrap 


 ## Created the keyspace and the required table in cassandra using the following commands.
       Create a keyspace in cassandra using the following command.
        CREATE KEYSPACE student_info WITH replication = {'class': 'SimpleStrategy', 'replication_factor': 1};
      
  ## Use the created keyspace.
      	USE student_info;
      
   ##   Created a table in cassandra using the following command.
        CREATE TABLE student (
	      id text PRIMARY KEY,
	      student_number text,
	      gender text,
	      birth_date timestamp,
	      disability boolean,
	      first_name text,
	      last_name text,
	      email text
        );
 
 ## Configured Cassandra instance details in "config.properties" file in the location "{Project_Directory}/src/main/resources".

      i)   cassandra.contactpoints - node addresses of the Cassandra instance.
      ii)  cassandra.port          - Hosted port number (Default port number is: 9042).
      iii) cassandra.keyspace      - The name of the database to be used (Default value is set to 'student_info').
	
 ## To Navigate to project directory containing the "pom.xml" file and run the following command.
      $ mvn clean install

 ## Deployed  to JBoss

 ## To access Use the following URL format for the deployed application.
      http://{Host_Name}:{Port}/App/
