## WEEK 14 HOMEWORK: Reverse Engineering, Code Break Down:
-   This weeks homework requires me to analyse a functioning application and break down its inner components to gain an understanding of it and how it works.


## Develop Folder:
## config:
- The file named config.json is a simple auto-generated document that is generated upon lanuch of the application. This application also mentions that this application uses 3 mySql databases. 
- The file named passport.js is the JavaScript element for the sign in portal. It simply checks whether or not the users email and password is valid, if it is not vaild the user is prompted with the following messages. "Incorrect email." and or "Incorrect Password."
-   Additionally, The config folder contains a branch folder called "middleware". This branch folder contains isAuthenticated.js, this file simply checks whether or not the user is signed into the application.
- This file will also redirect the user to a different route. That route being the sign in portal. 


## models:
-   Firstly, it is clear that the file named index.js is utilising sequelize to initalise a database, this index.js file also uses the config.json file which was covered earlier, it now servers as a module to link reference the databases. 
-   Secondly, the file named user.js is stores a user hashed password in one of their databases. The file also uses bcrypt to encrypt user passwords to strengthen their security.


## public: 
-   The name of this folder bascially explains its purpose and contents. Everything inside of this folder are the components that the user will be able to see and interact with. Such as the css, js, and html. 
-   The "js" folder contains 3 JavaScript files named "login.js", "members.js" and "signup.js". These provide the functionality for the 3 html files.
-   The folder contains 3 html files named "login.html", "members.html" and "signup.html". These 3 html files are the structure of the applications webpage. Each html file is different in purpose and function and they link with the JavaScript files detailed above. 
-   Lastly, the folder named "stylesheets" contains the css file which adds extra stylistic features to a webpage. 


## routes:
-   Finally, the folder titled "routes" is once again pretty self-explanatory, "routes" in JavaScript terms is the process of moving packets of data from a source to a destination, and in this application it moves data based on user requests. 
-   The folder also contains 2 files named "api-routes.js" and "html-routes.js". Firstly, I think "api-routes.js" collects data about the user and is client sided. It also has similar sections of code to "passport.js".
-   Lastly, "html-routes.js" is used to assist the computer with completing a user request based off of what it recieves from the user. For example, if it recieves a request of "/members" the computer checks to see if the user is signed in with "isAuthenticated", from here the computer will send the user through to the members page only if they are signed in, if the user is not signed in they are sent back to the sign in page. 



