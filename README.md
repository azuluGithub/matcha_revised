<h1> Matcha </h1>

```diff
# Is a WeThinkCode_ project.
```

<hr />

<h2> Description </h2>

 ```diff
 + This project is about creating a dating website.
 + The app allows two potential lovers to meet, from the registration to the final encounter.
 + A user is able to register, connect, fill his or her profile, search and look into the profile of other users, like them, chat with those that "liked" back.
```
<hr />

<h2> Features </h2>

```diff
- Registration and Signing-in
- User profile
- Browsing
- Research
- Profile of other users
- Chat
- Notifications
```
<hr />

<h2> Stack / Languages</h2>

<h3> Front-End: </h3>

```diff
# JavaScript (ES6+)
# React JS
# Redux
# HTML
# CSS
# Bootstrap
```

<h3> Server: </h3>

```diff
# Node JS
# Express JS
```
  
<h3> Back-End: </h3>

```diff
# Postgres SQL database
# Knex JS
# Cloudinary database
```

<hr />

<h2>Front-End NPM Packages</h2>
<em>for package versions: npm install package_name</em>

 <ul>
    <li>
      <em>
        <strong>
          leaflet && react-leaflet:
        </strong>
       </em>
    </li>
    
```diff
# map display
```
    
   <li>
      <em>
        <strong>
          moment:
        </strong>
       </em>
    </li>
    
```diff
# time conversion
```

   <li>
      <em>
        <strong>
          react-redux:
        </strong>
       </em>
    </li>

```diff
# connecting redux to react app
```

   <li>
      <em>
        <strong>
          react-router-dom:
        </strong>
       </em>
    </li>
    
```diff
# front-end routing e.g "/dashboad"
```

  <li>
      <em>
        <strong>
          react-scroll-to-bottom:
        </strong>
       </em>
    </li>
    
```diff
# provides a scrollbar component
```

   <li>
      <em>
        <strong>
          redux:
        </strong>
       </em>
    </li>
    
```diff
# global state of an application
```

  </ul>
  
<hr />

<h2>Back-End NPM Packages</h2>

  <ul>
    
   <li>
      <em>
        <strong>
          bcrypt-nodejs:
        </strong>
       </em>
    </li>
    
```diff
# password hashing, encryption and decryption
```

   <li>
      <em>
        <strong>
          body-parser:
        </strong>
       </em>
    </li>
    
```diff
# extracts the entire body portion of an incoming request stream and exposes it on req.body.
```

   <li>
      <em>
        <strong>
          cors:
        </strong>
       </em>
    </li>
    
```diff
# Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources on a web page to be requested from another domain outside the domain from which the first resource was served.
```

  <li>
      <em>
        <strong>
          cloudinary:
        </strong>
       </em>
    </li>
    
```diff
# cloud database that store images
```

  <li>
      <em>
        <strong>
          dotenv:
        </strong>
       </em>
    </li>
    
```diff
# used with .gitignore to hide configurations and api keys from being shared on github
```

  <li>
      <em>
        <strong>
          express:
        </strong>
       </em>
    </li>
    
```diff
# for creating a server and back-end routing
```

  <li>
      <em>
        <strong>
          express-form-data:
        </strong>
       </em>
    </li>
    
```diff
# sends form to the server
```

  <li>
      <em>
        <strong>
          knex:
        </strong>
       </em>
    </li>
    
```diff
# connects to database to store or fetch data
```

  <li>
      <em>
        <strong>
          nodemon:
        </strong>
       </em>
    </li>
    
```diff
# listens to file changes and restarts server during development if they are any changes made to the file
```

  <li>
      <em>
        <strong>
          nodemailer:
        </strong>
       </em>
    </li>
    
```diff
# sends email to the user after registration or request for password reset
```

  <li>
      <em>
        <strong>
          pg:
        </strong>
       </em>
    </li>
    
```diff
# postgres database stores information of all users
```

<li>
      <em>
        <strong>
          randomstring:
        </strong>
       </em>
    </li>
    
```diff
# works as string shuffle mechanism e.g to generate tokens used during email verification process
```

  </ul>

<hr />

<h2> RUNNING THE PROJECT </h2>

<h3> Requirements </h3>

<ul>
   <li>
      <em>
        <strong>
          Node js:
        </strong>
       </em>
    </li>
    
```diff
# Download nodejs to be able to run npm commands inside matcha app
```
   <li>
      <em>
        <strong>
          Postgres database:
        </strong>
       </em>
    </li>
    
```diff
# Download postgres to be able to store all user info for matcha app
```

  <li>
      <em>
        <strong>
          Cloudinary database:
        </strong>
       </em>
    </li>
    
```diff
# Enables you to store all app images
```

  <li>
      <em>
        <strong>
          Git:
        </strong>
       </em>
    </li>
    
```diff
# To use git commands e.g to clone the matcha project
```

</ul>

<em>Download nodejs here:</em> [node js!](https://nodejs.org/en/)<br />
<em>Download postgres database here:</em> [postgres database!](https://www.postgresql.org/download/)<br />
<em>Signup to cloudinary here:</em> [cloudinary database!](https://cloudinary.com/)<br />
<em>Download Git here:</em> [git!](https://git-scm.com/)

<hr />

<h2> Set Up Postgres </h2>

```diff
+ Open the SQL Shell
# Enter info e.g username and password to connect to the Database
```

<h3> Create database Matcha: </h3>

```diff
# CREATE DATABASE matcha;
```

<h3> Connect to Matcha: </h3>

```diff
# \c matcha;
```

<h3> Create tables: </h3>

```diff
# CREATE TABLE users (id serial PRIMARY KEY, firstname VARCHAR (100), lastname VARCHAR (100), username VARCHAR (100), email UNIQUE TEXT NOT NULL, photourl TEXT, img1 TEXT, img2 TEXT, img3 TEXT, img4 TEXT, gender VARCHAR (20), sexpref VARCHAR (20), age SMALLINT, bio TEXT, city TEXT, tags TEXT [], longi FLOAT, lati FLOAT, popularity SMALLINT, logged_time TIMESTAMP, is_logged_in BOOLREAN, active BOOLEAN, secrettoken TEXT);
+ CREATE TABLE views (id serial PRIMARY KEY, viewer TEXT, viewed TEXT);
- CREATE TABLE likes (id serial PRIMARY KEY, liker TEXT, liked TEXT, liketype SMALLINT);
+ CREATE TABLE matches (id serial PRIMARY KEY, user1 TEXT, user2 TEXT);
# CREATE TABLE chats (id serial PRIMARY KEY, sender TEXT, reciever TEXT, message TEXT, _time TIMESTAMP);
```

<h3> Exit: </h3>

```diff
# \q;
```

<hr />

<h2> Set Up Project </h2>

<h3> Clone Project: </h3>
[matcha project!](https://github.com/azuluGithub/matcha_revised)

<h3> STARTING PROJECT: </h3>

<h4> Navigate to back-end folder: </h4>

<ul>
   <li>
      <em>
        Create a 
        <strong>
          .env file 
        </strong>
        which should contain api keys:
       </em>
    </li>
    
```diff
# CLOUD_NAME = 'dsaj6ikxp'
# API_KEY = '187321199323491'
# API_SECRET = '2ZJFbRb5D1-bCgoDLvLUj_pRgmo'

# HOST = '127.0.0.1'
# USER = 'postgres'
# PASSWORD = 'rootadmin'
# DATABASE = 'matcha'

# GMAIL_USER = 'zuluarnold0@gmail.com'
# GMAIL_PASS = '143_50F7w@r3'
```
</ul>

<hr />

<h2>Pictures</h2>

<h4> Desktop Dashboard </h4>

![ddashboard image](/front_end/screenshots/dash_web.JPG)

<hr />

<h4> Mobile Dashboard </h4>

![mdashboard image](/front_end/screenshots/dash_mob.JPG)

<hr />

<h4> Profile </h4>

![profile image](/front_end/screenshots/prof_mob.JPG)

<hr />

<h4> Chat </h4>

![chat image](/front_end/screenshots/chat_mob.JPG)

<hr />

<h4> Other Users </h4>

![user image](/front_end/screenshots/user_mob.JPG)

<hr />
