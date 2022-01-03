# Verification-System

**INTRODUCTION**

A freeflow plugin which can be integrated with any CRM based on Django/Python based framework and allow products to integrate user verification. I did this project in my leisure time during undergrad and used Django-registration as a base application.

Basic Setup

```Pip install Django```

This line is used to start the project

```Django admin start-project verification```

Let’s create the app section in the project

```Python manage.py startapp registration```

Start the server

```Python manage.py runserver```

Make migration and migrate them

```Python manage.py makemigrations```

```Python manage.py migrate```

We import the classes that we are going to use to create our logic. This includes our signup form and token generator. We created our signup method in which we can access the input from the users and send it to the database.

We import django password token generators. This class generates a token to determine whether the token is valid or not. 

we create a method to activate a user account, in this method we pass uidb64 and a token which we will get from the url. we get the use from the database using the uid defined. if there is an error or a user does not exist in our database we return none. 

if the user exists and the token is valid, we set the user to active, and save the record .We login the user and we return a success message.We create the subject, message of our email and send it to the registered mail.

Then the user logs into the login account.

If the token is invalid, we notify the user that the link is not valid.
