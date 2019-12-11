<h1 align="center" style="font-size:300%;">
    <br>
    <br>
    Seenit  
    <br>
    <br>
</h1>

<h3 align="center">
    by
    <br>
    <br>
</h3>
<h2 align="center">
    Chaz Chang
    <br>
    Viet Dinh
    <br>
    My Nguyen
    <br>
    <br>
    TEAM 24
    <br>
    CS157A
</h2>

<p align="center">
  <a href="#project-description">Project Description</a> •
  <a href="#system-enviroment">System Enviroment</a> •
  <a href="#functional-requirements">Functional Requirements</a> •
  <a href="#non-functional-issues">Non-functional Issues</a> •
  <a href="#ERD Diagram">ERD Diagram</a> •
  <a href="#normalization">Normalization Processs</a> •
  <a href="#tables">Tables</a> •
  <a href="#implementation">Implementation</a> •
  <a href="#conclusion">Project Conclusion</a> •
</p>

# Project Requirements
## Project Description

### Overview:
The goal of this application is to create a rating site and discussion website. Users can be able to search and sort through posts. Also, users can create posts, comment on them, upvote, downvote, and save posts. In addition, users can join a channel and create channels that will function as communities. Users can view posts, view channels detail, view all channel, search and sort posts without logging in. However, to create posts, comment on them, vote and save posts, users are required to login. Moreover, users have to log in to view profile dashboard, delete account and update account. This application will allow people to easily voice their opinion or share a story. People can easily ask questions and others can answer them. It will also provide a user-friendly interface and fast response time while maintaining high throughput.

### Who would be interested in this application?
Users could be anyone who is interested in forming a community online, and interact with people with similar interests. Users can keep up to date with the daily life of others in their community. Companies and organizations can use Seenit to communicate with people and market products.

## System Enviroment
#### Structure of the system (graph based on 3-tiered architecture):




#### HW/SW used:
+ ReactJS
+ NGINX
+ Spring Boot
+ Windows/macOS
+ MySQL Workbench
+ Visual Studio Code
+ Slack
+ Github
  
#### RDBMS Used:
+ MySQL Version 5.6
  
#### Application languages:
+ Java (with Spring Boot framework)
+ SQL (with MySQL)
+ JavaScript (with ReactJS)
+ HTML/CSS

## Functional Requirements

### How users will interact with the system:
The application provides the same functionality for all the users. Internet connection is required for any activity on the system. A user shall be able to access the system for read and write. A user can access the system home page freely. They shall be able to read daily news and posts from various websites without logging in. Users can also be able to make a search based on their particular interests. However, users must log-in into the system and have their credentials checked for other activities such as make a new post, comment on a post, share a post and join another channel. First-time users must register for an account to perform the activities listed under log-in.

### Describe each individual function, functional process and I/O:
### Functions

#### I. WITHOUT LOGING IN, USERS CAN PERFORM THESE FUNCTIONS

#### Search 
+ The users shall be able to search for posts by post's title or its content. All the posts will be dispayed when its title or content contained the words in the search box.
+ If there is no matching results, nothing will be displayed.

#### Sort
+ Using to sort the posts by Top, New or None
+ Sort by Top will sort the posts by the upvotes they have.
+ Sort by New will sort the posts by date in descending order.
+ Sort by None means the result is random based on the data return from the endpoint.
+ User can active the function simply by selecting from a sort drop down menu 

#### View a post
+ By clicking on any post, users shall be able to see its contents and all the comments associated with it.

#### View a channel details
+ By clicking on a channel under Top channel, users shall be able to see all the post on this channel. Especially, users can see the moderator and channel details which including name of the channel and number of members.

#### View all channels

#### II. SIGN IN and SIGN UP FUNCTIONS

#### Log-in
+ Returning users must sign-in to perform the following activities: 
	+ View profile dashboard
	+ update the account
	+ Create a channel
	+ Join a channel
	+ Comment on a post
	+ save a post
	+ vote someone else's posts
	+ delete an account
+ To log in, users must enter their username or email and their password.
+ The system shall check the users' credentials. If the entered information is not matching with the information stored in database, an error message will be displayed. Otherwise, the system gives users access when the information is matching.

#### Register for an account
+ There will be only one type of user; no admin account in this application. First time user must sign up for an account to perform those activities listed in log-in function.
+ There will be a redirect link. User will be asked to fill out some information such as username, email address and password.
+ The system shall check if entered username is already existed. The system shall keep asking the users to enter a username until the name is available. Then, the system shall add the users' personal information into database.
+ The system shall check if entered email is already existed.

#### III. LOG-IN IS REQUIRED FOR THESE FUNCTIONS

#### View profile dashboard
+ Users can see all the posts and comments they have made.
+ They can also check the upvoted and downvoted posts as well as their saved posts. 
+ Any change in the database, for instance, comments added to a post and upvoted or downvoted are made, will be updated in the profile dashboard.

#### Join a channel
+ Without logging in, users will get a message syaing that they need to log in to join a channel.
+ The users shall be able to join a channel that they are interested in. 
+ This function is important for creating a post.
+ The system shall add the changes to database to keep track of the channels that a user joined.

#### Create a post
+ The user must join at least one channel to be able to create a post.
+ Title and content of the post are required before users hit the submit button. The created posts will be visible on the chosen channel.
+ The system shall save all the contents in the database after posting is finished.

#### Comment on a post
+ Without logging in, users will get a message syaing that they need to log in first to comment on a post.
+ The users shall be able to leave multiple comments on someone else's posts. Type what they want to say in the reply box, and hit post comment.
+ Once a comment is submitted , the data will be saved in database. Users can check the comments by viewing that post. They can also check all comments that they have made on the profile dashboard under Comments.

#### Save a post
+ Without logging in, users will get a message syaing that they need to log in first to save any post.
+ Otherwise, they can be able to save that post if they are interested in a particular postThe saved posts will be automatically added to their profile.
+ By saving a post, users can always go to their profile to continue reading or comment on the posts.

#### Upvote

#### Downvote

## Non-functional Issues
### Graphical User Interface (GUI): 
There are many design principles when it comes to web design. For our website, we will use seven most popular principles, which are Visual Hierarchy, Divine Proportions, Hick's Law, Fitt's Law, Rule of Thirds, Gestalt Design Laws, and White Space and Clean Design.

+ Visual Hierarchy: Certain parts of our website will be more important than others. We want to make those parts easily been seen and noticed by users. For example the account button, the scrolling posts, the filters, and the search box.
+ Divine Proportions: The layout, the size of each components should follow the golden ratio which is 1.618. For example, if the layout width is 1200px, the width of the content area should be 742px.
+ Hick's Law: "Hick’s Law says that with every additional choice increases the time required to take a decision." So, we plan to minimize the options for dropdown menu buttons. This will encourage new users trying new functions.
+ Fitt't Law: Button's size needs to follow a set of rules. The size of the button is proportion to its using-frequency.
+ Rule of Thirds: Since our website will allow users to upload pictures. The size of a picture needs to follow the rule of thirds to make it more interesting.
+ Gestalt Design Laws: Filter buttons, sorting buttons will be grouped together. Buttons will have consistent sizes.
+ White Space and Clean Design: Website without white/blank space is hard to navigate. So, we will use white space to divide the components, boxes that have different functions.
  
### Security
+ User accounts need to be highly protected. We don't want their personal information leaked or hacked.
+ Passwords are not stored in blank text. During user registration, passwords are hashed and salted using BCrypt before storing in the database. During login, the hashed passwords are compared
+ Sessions are handled with JWT (JSON Web Tokens). When users log in, they are given a JWT to send for future requests. The backend uses the JWT Signature to see if the JWT is valid. The JWT Signature makes it more difficult for a malicious user to pretend to be some other user.


### Access Control
+ Anyone with internet can access the website
+ A user will be able to view posts/channels and search without logging in
+ A user must login to create posts, comments, or channels
+ A user cannot edit posts or comments that belong to a different user
  
### Performance
+ Fast response time while maintaining high throughput
+ The MySQL database will be optimized so queries don't take too long. The right data types and efficient SQL queries will make the database accesses faster and the database size smaller
+ ReactJS will be used to build the User Interface. ReactJS will allow the user to navigate through the application quickly by dynamically changing the current page instead of loading a whole new page from the server
  
### Scalability
+ Able to add new functions and features while developing the app

# Project Design

### Update ERD
INSERT PICTURE

#### List all completely non-trivial FDs that apply to your design. 

#### Convert ER to schemas
+ Users(​id​, email, username, password, created_at, avartar_url)
+ Posts(​id​, title, content, created_at, updated_at)
+ Comments(​id​, content, created_at, updated_at)
+ Channels(​id​, name, banner_url) 

+ Create_Post(​user_id​, ​post_id​, points)
+ Create_Com(​user_id​, ​com_id​,points)
+ Have(​post_id​, ​com_id​)
+ Have_Com(​parent_id​, ​child_id​)
+ Save(​user_id​, ​post_id​)
+ Vote_Post(​user_id​, ​post_id​, up_down)
+ Vote_Com(​user_id​, ​com_id​, up_down)
+ Contain(​post_id​, ​channel_id​)
+ Own(​user_id​, ​channel_id​)
+ Moderate(​user_id​, ​channel_id​)
+ Subscribe(​user_id​, ​channel_id​)

#### Explanation for each entity set and relationship, write a short description in plain English of what it represents or models.
Entity sets​:
+ Users: has ID number (PK), email, username, password, points, created_at, and avatar_url (image url). Stores user data
+ Posts: has ID number (unique), title, content, created_at, and updated_at. Stores Post data
+ Comments: has ID (PK), content, created_at, and updated_at. Stores comment data in a Post.
+ Channels: has ID (PK), name, and banner_url(image banner). Channel is also represented by unique id. Stores channel data

Relationships:
+ Own: has a channel_id and user_id. Stores who owns which channels
+ Moderate: has a channel_id and user_id. Stores who moderates which channels
+ Subscribe: has a channel_id and user_id. Stores who subscribes to which channels
+ Contain: has a channel_id and post_id. Stores which channels contain which posts
+ Create_Post: has post_id, user_id, and points. Stores which posts are created by which users. Also stores the number of points a post has
+ Create_Com: has comment_id, user_id, and points. Stores which comments are created by which users. Also stores the number of points a comment has.
+ Vote_Post: has post_id, user_id, and up_down. Stores which posts are voted up or down by which users
+ Vote_Com: has comment_id, user_id, and up_down. Stores which comments are voted up or down by which users
+ Save: has user_id and post_id. Users can share a post to save it so that they can read the post again later.
+ Have: has post_id (parent) and comment_id (child). Stores which posts have which comment replies
+ Have_Com: has comment_id1 (parent) and comment_id2 (child). Stores which comments have which comment replies

### Perform the normalization process, and perfect the relational database schemas to BCNF

### Create and show at least 10 tables according to schemas and model the data stored in the database (Each table must contains at least 15 tuple instances.) 

# Implementation

### Detail explanations of how your DB application system was implemented.
We have the front-end handled by React framework. With React, we just need to know the basics of HTML and CSS. There are a few css libraries that we use such as Material-UI and styled-components. These libraries help us build a better dynamic and responsive UI. At the front-end, we also use Redux for state management. One of the hardest parts in building the front end is state management. There is a lot of overhead when using Redux, but without Redux, when the app getting bigger, it will be super hard to be maintained. To communicate with the backend, the front-end will use fetch() function, which supports all the HTTP methods. We use Spring Boot to build our Rest API, which will handle all the logics and communicate to MySQL database. To connect with MySQL, we just need to add the connector dependency to the Pom file. Working with MySQL using Object mapping created a big overhead. There are not many tutorials on mapping Java class to tables. I spent a few weeks just to do research on mapping. This part is the hardest part when building our backend. The end result is great because it super simple to query and modify the database. We can treat tables like classes. All the mapped classes are in the “model” folder. We don’t need to create a model for a relationship that doesn’t have extra attributes. For database manipulation, we use JPA Data framework, which support both native SQL query and JPQL query. To do that we just need to create an interface that extended JpaRepository interface and inject a @Repotory Bean to the interface. If we want to get all posts from Post table using JPQL, we can do:
```bash
@Query(“SELECT p FROM Post”)
List<Post> findAllPostCustom();
```
The syntax is really similar with native SQL. To write out endpoints, we inject @RestController Bean to our classes. To write a GET request, we inject @GetMapping(<url name>) and to write Post request, we do @PostMapping(<url name>). The syntaxes will be similar for DELETE, and PUT. With Spring Boot, creating endpoints is really simple and quick. We also add security to our backend using spring-boot-starter-security library. 


### Keep tracks of implementations from design
 
+ Identify the entities, attributes, dependences, relationships, constraints, etc. (show screenshots of  corresponding tables, GUI, execution results, and so on.)

+ Show functions/features associated with query, insertion, updating, and deletion operations. (Screenshots)

+ Procedures (step by step) of how to set up and run your system
<h1 align="center">
  <br>
  <br>
    Seenit 
  <br>
</h1>

<h4 align="center">A Reddit clone using <a href="https://reactjs.org/" target="_blank">React</a>, <a href="https://spring.io/" target="_blank">Spring Boot</a>
and <a href="https://www.mysql.com/" target="_blank">MySQL</a></h4>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-try-locally">How to Try</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a>
</p>


## Key Features 

## How To Try Locally

### Requirements:
+ [Git](https://git-scm.com)
+ [Node.js (version >=10.0.0)](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com))
+ JDK (version >=1.8)
+ Maven (version >=3.2)
+ Spring-2.1.8 RELEASE
+ MySQL (version >=5.1.47) 
  
**If you use an approriate IDE, you dont need to manually install Maven and Spring.** 

**From your command line:**

```bash
# Clone this repository
$ git clone https://github.com/CS157A-Team24/Seenit
$ cd Seenit
```
**Client side**
```bash
# Go into the client repository
$ cd client

# Install dependencies
$ npm install or yarn install

# Run the app
$ npm start or yarn start
```
In case the website doesn't automatically pop up, go to http://localhost:3000/


**Server side**

Simply use an IDE such as IntelliJ and NetBeans, import/open the project and hit "run" or if you refer command line:
```bash
# Go into the server repository
$ cd server

# Compile and run
$ mvn spring-boot:run
```
Default port at http://localhost:8080/. Configurate the *application.properties* file to match your MySQL server address if it isn't at localhost:3306. 
Note: You can use our public database server which is already setup, so you don’t need to modify anything

**Database**

Start your MySQL server. Create the Databse and Tables using the SQL files in *database* foler. 

## Credits

This software uses the following open source packages:

- [Node.js](https://nodejs.org/)
- [React](https://reactjs.org/)
- [Spring Boot](https://spring.io/)

## License


# Project Conclusion

### Statements from each team member about Lesson Learned from this DB project

Viet Dinh: I have built many web applications using React, but not Redux. I tried Redux before but had never built something the size of our project. After finished our project, I have more confidence to use Redux and I really like it. Debugging the state of React using Redux is amazing. This is my first time using Spring Boot, the reason why I chose Spring Boot is because I did some research and found out it really simple to work with SQL databases. Although it has a lot of overhead to map classes to tables when there is a relationship that has extra attributes, it really simple to communicate with database from there. I learn to build a better Rest API using Spring Boot that can store data to a database server. The important lessons I learned from this class are how to use MySQL database, design and manage database.

### Future improvement of your DB application
