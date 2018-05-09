# Intl.Intern
## An Internship tracking tool

## Table of Contents
* [View Live Site](#view-live-site)
* [About this project](#about-this-project)
* [Getting started](
* Structure of the project
* Technologies used

## <a name="view-live-site"></a> View Live Site

## <a name="about-this-project"></a> About this project
* [How It Works](#how-it-works)
* [Technologies Used](#technologies-used)
* [Start Locally](#start-locally)

## <a name="how-it-works"></a> How It Works
1. Create Profile
* Create a user profile with details of your home location and internship locations such as city, country and currency code. 

2. Jornal Page
* Keep track of milestones hit and requirements met by creating chapters in your personal journal page:
    * Add a chapter by entering a title, description and date. Additional optional fields include a picture and requirement number met
    * Delete a chapter
    
3. Expenses Page
* Keep track of expenses throughout your internship :
    * Log expense in US dollars or local currency using the expense tracking form
    * View a day-by-day ledger with both local currency and US Dollars noted or a graphical representation of expenses by week
    
4. Location Page
* View information about your internship location. Available information includes:
    * Local Map
    * Local Weather
    * Currency exchange rates
    * Timezone information
    * New York Times News 
    
5. Requirements Page
* Keep track of internship requirements set by your university or self by creating them on your requirements page
    * Add a requirement by entering a title and description
    * Conveniently view requirements below your pages on the side navigation

## <a name="technologies-used"></a> Technologies Used
* FRONTEND
    * HTML
    * CSS
    * Material-UI
    * Javascript
    * React

* BACKEND
    * Yarn Packages 
        * Chartist.js
        
    *  APIs Used
        * CurrencyLayer
        * GoogleMaps
        * NYTimes
        * OpenWeather

## <a name="start-locally"></a> Start Locally
1. Clone the repository
Start by cloning this project to a local directory on your computer. Run the following commands
```
git clone https://github.com/jstudenski/project-three
```
2. Structure of the project
After you clone the reposity, navigate to the root directory (project-three). The project directory structure is set up as follows: 

* Server.js: This file:
    * Defines and requiers the dependencies, including express, body-parser, morgan logger, mongoose, passport
    * Sets up the Express server
    * Sets up the Express server to handle data parsing use body-parser
    * Sets up the logger
    * Sets up passport
    * Points the server to the API routes
    * Defines the port the server is listening on
    * Starts the server
    * Allows the app to serve static conten from the public directory

* models: Contains chapter.js, expense.js, index.js, needs.js and user.js files which contain the information for the application to set up the database

* controllers: Contains chaptersController.js, countryConroller.js, expenseController.js, needsController.js and usersController.js which contain the information fo the various pages for the application to interact with the database

* routes: Contains API folder and index.js file
    * API folder contains chapters.js, country.js, expense.js, index.js, needs.js and user.js files that sets up routers for each page
    * index.js file compiles all the routes for the app to use
    
* scripts: Contains the build.js, seedDB.js and start-client.js generated by create-react-app

* client: Containts public and src folders
    * public: Contains generated documents from create-react-app
    * src: Contains components file, pages file, utils file, App.js, index.js, index.css, country_codes.json, currencycodes.json, city-list.json
        * Components : Contains folders for each React component including, Forms, Sidebar, Login, TopNav and Users
        * Pages: Contains folders with files for each page of the application including Journal, Expences, Location, Requirements and NoMatch
        * Utils: Contains API.js, util.js
            * API.js: Contains API calls the database for each page, API calls for images and NYTimes search
            * util.js: Contains API calls for OpenWeather API
    


3. Install front and backend dependencies. Whle in this directory, run the following command:
```
yarn installDeps
```






This setup allows for a Node/Express/React app which can be easily deployed to Heroku.

The front-end React app will auto-reload as it's updated via webpack dev server, and the backend Express app will auto-reload independently with nodemon.

## Starting the app locally
Start by installing front and backend dependencies. While in this directory, run the following commands:
```
yarn install
cd client
yarn install
cd ..
```

After both installations complete, run the following command in your terminal:

```
yarn start
```

That's it, your app should be running on <http://localhost:3000>. The Express server should intercept any AJAX requests from the client.


