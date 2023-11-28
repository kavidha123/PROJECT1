# PROJECT1

THIS PROJECT IS TAKING A LOT OF TIME SO BASED ON YOUR REQUIREMENTS IAM GIVING YOU DETAILS WHAT HAS TO BE DONE BASED ON CODING .
 
YOUR REQUIREMENT IS :
As a next step, we expect you to complete a short assignment.
1. Create a backend tier using ExpressJS.
2. Create a PWA using React that that accepts text input (ID), a photo, text input (friendID) and password, and sends it to the backend.
3. The backend server should have the following 3 functionalities -
a. log the number of times a connection is made by the frontend and insert it into a Mongoose Model
b. receive the text that was inserted from the frontend and insert it in another Model and Table
c. calls the Django api using the most recent 2 strings and returns the ngrams to the frontend
d. Add the persons ID (A) to mongodb
e. store the encrypted photo in a directory on the disc using multer (A)
f. update friend's (B) friendList to include person (A)
4. Create a Django server that has an API that returns the ngrams comparison using NLTK.
5. Create a new repo on GitHub which has all the commits, independent branches for the 3 pipelines that are merged for submission.
6. Bonus : Containerise each of the components on independent docker containers

Submission should include the following - 
a. maximum 4 minute video demonstrating the functionality and walkthrough of the code. Make sure you are audible.
b. Link to GitHub repo complete with a proper readme and a task checklist. 

Evaluation criteria - You'll be judged on the basis of - 
a. Number of tasks completed
b. Your speed 



THE BASIC STRUCTURE OF THE PROJECT IS
1. Backend Tier with ExpressJS
You'll need to set up an ExpressJS server that connects to a MongoDB database using Mongoose. Your server will have various routes and controllers to handle different functionalities.

Server Setup (server.js):

Initialize an Express app.
Connect to MongoDB using Mongoose.
Set up middleware (e.g., body-parser, multer for file uploads).
Define routes.
Models (/models):

ConnectionLog.js: Schema for logging connections.
TextEntry.js: Schema for storing text entries.
User.js: Schema for user information, including friend lists.
Routes (/routes):

connectionRoutes.js: Routes for connection logging.
textRoutes.js: Routes for handling text entry.
userRoutes.js: Routes for user operations.
ngramRoutes.js: Routes to interact with Django backend.
Controllers (/controllers):

Implement logic for each route.
Utilities (/utils):

multerConfig.js: Configuration for multer to handle file uploads.
encryption.js: Utility for encrypting data.
Database Configuration (/config):

mongoose.js: Configuration for MongoDB connection.
2. Frontend with React (PWA)
Create a React application that can send data (including files) to the backend.

React App Structure (/src):

Components/FormComponent.js: Component to take inputs (ID, friendID, photo, password).
Services/apiService.js: Service to interact with the backend.
App.js: Main app component.
index.js: Entry point of the React app.
Public Folder (/public):

index.html: Main HTML file.
manifest.json: For PWA configuration.
serviceWorker.js: Service worker for offline capabilities.
3. Django Backend for N-grams Analysis
Set up a Django project that exposes an API endpoint for n-gram analysis.

Django Project Setup (/ngram_project):

Initialize a Django project.
Django App (/ngram_app):

models.py: Define any models if needed.
views.py: Logic for handling n-gram analysis.
urls.py: URL patterns for the n-gram API endpoint.
Utilities:

ngramAnalysis.py: Utility for performing n-gram analysis using NLTK.

FRONT END Setting up the React Project

npx create-react-app my-pwa
cd my-pwa
Running the App: To run the app, use npm start in the project directory.

 ExpressJS Backend

Initialize a new Node.js project with npm init.
Install ExpressJS (npm install express) and Mongoose (npm install mongoose) for handling MongoDB interactions.
Optionally, install multer for handling file uploads (npm install multer).



Django Backend for N-grams Analysis


Django Project Setup (/ngram_project)

pip install django


django-admin startproject ngram_project
cd ngram_project

python manage.py startapp ngram_app


pip install nltk

 Running the Server

python manage.py runserver


After defining these models, remember to perform migrations to create the corresponding tables in your database:

python manage.py makemigrations
python manage.py migrate





