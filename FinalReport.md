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
  <a href="#non-functional-issues">Non-functional Issues</a>
</p>

# Project Requirements
## Project Description

### Overview:
The goal of this application is to create social news, rating site, and discussion website. Users can be able to check daily news, search, filter, and sort through posts. Also, users can create posts, comment on them, like, and share posts. In addition, users can create channels that will function as communities. Users can view posts without logging in, but creating posts, commenting, and liking will require the user to login. This application will allow people to easily voice their opinion or share a story. People can easily ask questions and others can answer them. It will also provide a user-friendly interface and fast response time while maintaining high throughput. 

### Who would be interested in this application?
Users could be anyone who is interested in forming a community online, and interact with people with similar interests. Users can keep up to date with news, information, and ideas in their community. Companies and organizations can use Seenit to communicate with people and market products.

## System Enviroment
#### Structure of the system (graph based on 3-tiered architecture):




#### HW/SW used:
+ ReactJS
+ NGINX
+ Spring Boot
+ Windows/macOS
+ MySQL Workbench
+ Visual Studio Code
  
#### RDBMS Used:
+ MySQL Version 5.6
  
#### Application languages:
+ Java (with Spring Boot framework)
+ SQL (with MySQL)
+ JavaScript (with ReactJS)
+ HTML/CSS

## Functional Requirements

### How users will interact with the system:
The application provides the same functionality for all the users. Internet connection is required for any activity on the system. A user shall be able to access the system for read and write. A user can access the system home page freely. They shall be able to read daily news and posts from various websites without logging in. Users can also be able to make a search based on their particular interests. However, users must log-in into the system and have their credentials checked for other activities such as make a new post, comment on a post, share a post, create a channel, and follow another channel. First-time users must register for an account to perform the activities listed under log-in. 

### Describe each individual function, functional process and I/O:
### Functions

####I. WITHOUT LOGING IN, USERS CAN PERFORM THESE FUNCTIONS

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

#### View a channel details

#### View all channels

####II. SIGN IN and SIGN UP FUNCTIONS

#### Log-in
+ Returning users must sign-in to perform the following activities: 
	+ create chanel
	+ access profile page
	+ create a new post
	+ like or comment on someone else's posts
	+ save a post
	+ join channel
+ Guests or unregistered users can only search posts, sort posts on the main page, view a channel, and view posts.
+ The system shall check the users' credentials. If the entered information is not matching with the information stored in database, an error message will be displayed. Otherwise, the system gives users access when the information is matching.

#### Register for an account
+ There will be only one type of user; no admin account in this application. First time user must sign up for an account to perform those activities listed in log-in function
+ There will be a redirect link. User will be asked to fill out some information such as first name, last name, email address, username, and password. 
+ No limitation. Users can set up multiple accounts and choose which one to log-in with depending on the personal channel which users want to participate in. 
+ The system shall check if entered username is already existed. The system shall keep asking the users to enter a username until the name is available. Then, the system shall add the users' personal information into database.

####III. LOG-IN IS REQUIRED FOR THESE FUNCTIONS

#### View profile dashboard
+ Users can see all the posts and comments they have made.
+ They can also check the upvoted and downvoted posts as well as their saved posts. 
+ Any change in the database, for instance, comments added to a post and upvoted or downvoted are made, will be updated in the profile dashboard.

#### Setting
+ Users shall be able to update the email.
+ Users shall be able to update the password.
+ Users shall be able to delete an account.

#### Create a channel 
+ Once users are signed in, users can create their own channels. On their channel, users are able to 
+ Users can create multiple channels (up to 4). By creating a channel, a user can get followers who are interested in his/her activities.
+ The system shall save information of the channel in database.

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

#### Delete

## Non-functional Issues
### Graphical User Interface (GUI): 
There are many design principles when it comes to web design. For our website, we will use seven most popular principles, which are Visual Hierachy, Divine Proportions, Hick's Law, Fitt's Law, Rule of Thirds, Gestalt Design Laws, and White Space and Clean Design.

+ Visual Hierachy: Certain parts of our website will be more important than others. We want to make those parts easily been seen and noticed by users. For examples the account button, the scrolling posts, the filters, and the search box.
+ Divine Proportions: The layout, the size of each components should follow the golden ratio which is 1.618. For example, if the layout width is 1200px, the width of the content area should be 742px.
+ Hick's Law: "Hick’s Law says that with every additional choice increases the time required to take a decision." So, we plan to minimum the options for dropdown menu buttons. This will encourage new users tring new functions. 
+ Fitt't Law: Button's size needs to follow a set of rules. The size of the button is proportion to its using-frequency.
+ Rule of Thirds: Since our website will allow users to upload pictures. The size of a picture needs to follow the rule of thirds to make it more interesting. 
+ Gestalt Design Laws: Filter buttons, sorting buttons will be grouped together. Buttons will have consistent sizes. 
+ White Space and Clean Design: Website without white/blank space is hard to navigate. So, we will use white space to divide the components, boxes that have different functions. 
  
### Security
+ User accounts need to be highly protected. We don't want their personal information leaked or hacked. 
+ Passwords won't be store in blank text, it will be hashed. 
+ We will use https protocol for our web server to make sure the connection between users and server are encrypted. 
  
### Access Control
+ Anyone with internet can access the website
+ A user will be able to view posts/channels and search without logging in
+ A user must login to create posts, comments, or channels
+ A user cannot edit posts or comments that belong to a different user
  
### Performance
+ Fast response time while maintaining high throughput
+ The MySQL database will be optimized so queries don't take too long. The right data types and efficient SQL queries will make the database accesses faster and the database size smaller
+ ReactJS will be used to build the User Interface. ReactJS will allow the user to navigate through the application quickly by dynamically changing the current page instead of loading a whole new page from the server
+ NGINX can be used as a load balancer but it will require money for more resources like computers and databases. We won't use many resources during this semester, but this makes it  scalable for later
  
### Scalability
+ Able to add new functions and features while developing the app
+ NGINX will be used on the web server. NGINX can be used as a load balancer to distribute the work over many computers. Load balancing will help create high throughput and low response time by avoiding overloading a single computer. NGINX will allow more computing resources (CPU and memory) to be easily added to the existing system.

# Project Design

### Update ERD

### Perform the normalization process, and perfect the relational database schemas to BCNF

### Create and show at least 10 tables according to schemas and model the data stored in the database (Each table must contains at least 15 tuple instances.) 

# Implementation

### Detail explanations of how your DB application system was implemented.

### Keep tracks of implementations from design
 
+ Identify the entities, attributes, dependences, relationships, constraints, etc. (show screenshots of  corresponding tables, GUI, execution results, and so on.)

+ Show functions/features associated with query, insertion, updating, and deletion operations. (Screenshots)

+ Procedures (step by step) of how to set up and run your system

# Project Conclusion

### Statements from each team member about Lesson Learned from this DB project

### Future improvement of your DB application
