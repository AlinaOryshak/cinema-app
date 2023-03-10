<h1 align="center">
 Cinema App 
:film_projector:
:popcorn:
</h1>

<h2>
:pushpin: Description
</h2>

> A RESTful application that is designed according to SOLID principles.
> It is based on the combination of Spring and Hibernate frameworks 
> to achieve Inversion of control and also quick and safe communication with DB.
> In addition, using DTOs permits to show only necessary and non-sensitive information. 
>
> App allows you to register or log in for performing different operations due to your role.
> For example, you can manage movie sessions, movies and cinema halls information as an admin.
> Or you can search available movies, add tickets to your shopping cart and make the orders as a user.

___

## Content

<p>
<a href="#features">Features</a><br>
<a href="#project_structure">Project structure</a><br>
<a href="#technologies">Technologies</a><br>
<a href="#instructions">Instructions</a><br>
</p>

___

<h2 id="features">
:star: Features
</h2>

Registered and logged-in ***users*** have the following possibilities:
* getting cinema halls;
* getting movies;
* getting available movie sessions due to definite date;
* add movie sessions to their shopping carts;
* getting tickets from their shopping carts;
* completing orders;
* getting orders history;

Registered and logged-in ***admins*** have the following possibilities:
* adding/getting cinema halls;
* adding/getting movies;
* adding/updating/deleting movie sessions;
* getting available movie sessions due to definite date;
* finding users by their emails;

___

<h2 id="project_structure">
:derelict_house: Project structure
</h2>

Application is divided into logical layers in accordance with 3-tier architecture to separate responsibilities
and manage dependencies in project.

| Tier         | Responsibility                                                                                    |
|--------------|:--------------------------------------------------------------------------------------------------|
| Presentation | Uses Controllers to interact with users                                                           |
| Logic        | Uses Services to perform data processing and their transferring to other layers of an application |
| Data         | Uses DAOs to operate database and perform CRUD operations                                         |

<b><i>UML Class Diagram for Cinema application</i></b>

<img src="img/umlDiagram.png" alt="umlDiagram" width="600">

___

<h2 id="technologies">
:computer: Technologies
</h2>

* JDK 17
* Maven 3.3.2
* Spring 5.3.20
* Spring Web 5.3.20
* Spring Security 5.6.10
* Hibernate 5.6.14 Final
* MySql 8.0.22
* Tomcat 9.0.50
___

<h2 id="instructions">
:hammer_and_wrench: Instructions
</h2>

1. Install [Apache Tomcat](https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.50/bin/) if it's needed.
2. (Optional)  Install [MySQLWorkbench](https://dev.mysql.com/downloads/workbench/) to control changes in the database after request processing.
3. Clone this project from GitHub.
4. Change URL, username, password and JDBC driver in [db.properties](src/main/resources/db.properties).
5. Configure Tomcat server :
    * Press *Edit configuration*;
    * Choose *Tomcat Server (Local)*;
    * Go to *Deployment*
        * *Add -> Artifact -> taxi-service:war exploded*
        * *Application context -> /*
    * Press *Ok*.
6. Run the application.
7. Pay attention that the application creates admin with email `"admin@i.ua"` 
and password `"admin123"` by default in [DataInitializer](src/main/java/cinema/config/DataInitializer.java) class
after its launching.

<h3><b>GOOD LUCK !</b> :rocket:</h3>
