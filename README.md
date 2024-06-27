# Exercise-Tracking-App

Welcome to the Boat and Load Tracker API!

## Table of Contents
  - [Overview](#overview)
  - [App File Structure](#app-file-structure)
  - [Features](#features)
  - [Screenshots](#screenshots)
  - [Technologies Used](#technologies-used)
  - [Installation and Operation](#installation-and-operation)

## Overview

This is a full-stack MERN (MongoDB, Express.js, React.js, Node.js) application that allows a user to CRUD (create, read update and delete) their exercise routines.

## App File Structure
The following is a brief overview of the file structure


[./frontend](https://github.com/voyagerfan/Exercise-Tracking-App/tree/main/backend) - Contains components, pages, index and associated JSON files.

[./backend](https://github.com/voyagerfan/Exercise-Tracking-App/tree/main/frontend) - Contains model, controller and associated JSON files.

## Features
* The Excercise tracker implements model-view-controller architecture (MVC) for maintainability, scalability. 
* Being a single page application (SPA), the exercise tracker offers faster perceived performance for the user with smoother page transitions.

* **Front-end:**
  * A user can add an exercise record and customize attributes such as the "name", "reps", "weight", "unit", "date".
  * Each row record includes an icon for delete and edit to make the process straight forward and simple.
  * A confirmation alert is shown on the screen after each successful CRUD operation has been completed.
  
* **Back-end:**
  * REST API built with Node.js to facilitate interactions with data.
  * Integrates MongoDB (a NoSQL database) offering flexibility in storage.  

## Screenshots
Home Screen

![](./screenshots/homescreen.png)

Add Exercise Screen

![](./screenshots/add_exercise_screen.png)

New Exercise Added

![](./screenshots/new_exercise_added.png)

Edit an Exercise

![](./screenshots/update_screen.png)

Multiple Exercises

![](./screenshots/multiple_entries.png)



## Technologies Used

- **Programming Languages:** Javascript, HTML, CSS 
- **Frameworks:** Node.js, Express.Js, 
- **Database:** MongoDB

## Installation and Operation

*Prerequisites*: **MongoDB**, **Node.js**, an **IDE**

> [!IMPORTANT]
> The following instructions are intended for Visual Studio Code but feel free to use an IDE you are comfortable with. 

**1. MongoDB setup**
* You will need to create a [MongoDB account](https://account.mongodb.com/account/login). There is a free version you can sign up for.
* MongoDB documenation can be found [HERE](https://www.mongodb.com/docs/atlas/getting-started/?_ga=2.42031591.393924942.1718915988-924210838.1718915988&_gac=1.55707609.1718931935.CjwKCAjwps-zBhAiEiwALwsVYUhT__z-AiKBSj7jQbqW2niZsWsHbx0h1hWaw1SpILlvYBZteqeR5RoCkdYQAvD_BwE). Generally you will need to:
  * Start a new project
  * Deploy a cluster
  * Save your password
  * Save your connect string
    * Your connect string should look like this:
    * mongodb+srv://**user_name**:**password**@cluster0.7sl2w4i.mongodb.net/?retryWrites=true&w=majority&appName=**cluster_name**
  * Add your password to the connect string and save this for later.

**2. IDE Setup**

* Click on the "Exentensions" icon (left pane).
* Type MongoDB into the search bar. 
* Find "MongoDB for VS code". It should have a green leaf as an icon.
* Click install
* A grey leaf should be added to your list of icons in the left pane.
* Click on the grey leaf.
* Click on the "Connections" drop down menu.
* Click on the "+" sign. A screen should pop up asking to connect using a connect string or advanced connect.
* Click on "connect with connect string" 
* Add your connect sting with the password to the quick access bar (top search bar) of VS Code and press ENTER
* You should be connected now

**3. Configure the Exercise Tracking App**
* Clone the repo from the repository.
* Open the application folder in VS Code
* Install Node.js
  * It may be downloaded [HERE](https://nodejs.org/en/download/source-code)
  * Alternatively, you can open the terminal in VS Code and run the commands for the package manager. [This website](https://nodejs.org/en/download/package-manager) provides commands line arguments to install Node.js for different operating systems.
* In the terminal, navigate to ./backend
  * install node dependencies by opening a terminal in VS Code and run the following command.
   ```
   npm install node_modules
   ```
   *Note: The npm command will not work unless Node.js is installed properly.
* In the terminal, navigatve to ./backend/movies-rest
  * add a file called .env
  * In the file add the following
   ```
   MONGODB_CONNECT_STRING = 'Your connect string with password' 
   PORT = 8000
   ```

**3. Run the Application**
* Open 2 terminals in VS Code.
* In one terminal, navigate to ./backend/movies-rest
* enter the command
   ```
   npm start
   ```
* In the second terminal, navigate to ./frontend/movies-ui
* enter the same command
   ```
   npm start
   ```
* If a web page does not open immediately, open a browser and enter the following URL
  ```
  127.0.0.1:3000
  ```
* The webpage presented should look like the screen entitled "home screen"
