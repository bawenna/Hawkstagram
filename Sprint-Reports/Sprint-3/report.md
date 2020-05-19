## 1.Team members FunctionsBX
Akshay Patel (UI/UX Developer)

Hugo Zamarripa Vazquez (Project Manager)

Jingwen Yu (Jr. Developer)

Junhua Dong (Tom) (IT Operations)

Maryam Ibad (IT Operations)

Wenzhao Zhang (Developer)

## 2.Goals for this Sprint
---
1. Majority of the changes in this sprint came from **dropping** the use of **Cloudinary** API in our system.
The API already incorporated inside our logic was responsible with storing our pictures on a cloud server and providing our local database(mongo DB) with access to that data.
2. More priority working deployment of dev environment via packer script and vagrant.
3. Despite the set back we want to have 15 test users automated to use our web app.
4. Providing the documentation on how to configure deployment and run the dev environment and having all members of the project
5. Another goal we wanted to finally touch on more finely was security, we wanted to have backups of the database using MongoDB replica with our data
since we would now be more responsible for them as they are locally stored, and provide self signed certificates per requirement.

6. For the UI/UX we made our first completed version of the layout design, responsive design is our priority as a group so the phone views where modified first. Font, font
7. size, line height, background-color, overflow on scroll, and defining when the scaling at different widths would change at 960px, 640px, and 320px.
Creating a new site map with updated flowchart excluding Cloudinary.

---
## 3.Accomplished
Added a rough draft of responsive function to our design layout to add things like media screens
to scale the view on phones

Successfully added self signed certificates to our project, we can verify that it is a self signed certificate because the https goes to not secure as it is self signed.

Completely overhauled our previous iteration using Cloudinary and completely removed all references to the API.

Cloudinary overhaul
1. Now we are storing our images in a local folder
2. Under public / photos
3. All the metadata are stored in the photo schema in Mongo db
We kept logic function flow mostly the same since we are still using Node.js except now all
the metadata we extract is from mongo DB to match with, so searching for tags is still the same method.

As cleanup in terms of streamlining our dev environments we all have our deploy keys on the repository.
We also now have a working and running packer script to run our environment and instructions so
others can do the same, we move from Xenial to Vanilla as our main environment OS although that has not caused any
problems or changes to our development.

## 4.Changes to be made/not completed
1. We were not able to complete mongo db replication due to known bugs it is in progress and will be done
by next sprint

![alt text](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/image.png "Database_replication")

essentially our primary database called "users", and we are trying to replicate the primary database. As the users enter the data, the replicated database will copy the data from the primary database

2. The overhaul of cloudinary took priority so we were unable to redo the entire update sitemap with added
flow charts, we did want to do modular changes that can roll over without the need of a site map that aligned with our previous
goals of responsive design.

3. Creating 15 test users also took less priority and will be done in upcoming sprint once our web app is more stable.

4. Creating a search by tag with multiple tags is also on the backburner until next sprint because of the cloudinary set back as well
as known bugs.
---
## 4.Bug Tracking
Currently have two known bugs:
1. Once deployed on our environments any stored pictures will not show on web app,
but we can run the code all the way through with no error thrown.

---
## 5.Security Assumptions

Implementing self signing certificates

![alt text](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/ssl.PNG "Certificates")
---
## 6.Team Members Comments
Akshay Patel:
As a UI/UX designer I focused on how the website looked and how smooth it was on different screens. I first examined how our product felt, and we had a design problem on the website itself, also how the page flow was from one to another. Then for UI I wanted to see and test how our product was laid out, and fix anything that was in the wrong layout, and reporting the problems with the project manager, and solving them afterwards.  
Hugo Zamarripa Vazquez:

Jingwen Yu: As a Jr.developer, I focused on replication of the current database. I wanted to implement a replica set, but I was facing some issues of database connection and change the current standalone database type to a replica set database. 

Junhua Dong: As IT Operater, I mainly foucsed help to both developer and UI/UX designer to slove their technology problem including the code problem such as modefied function for connect with the db.

Maryam Ibad:
Being one of the IT Operations manager for this sprint, my main task included; making sure smooth functioning of our project's infrastructure and deployment environment. I was also assigned with the task of creating 15 test users that we need for testing purposes. 

Wenzhao Zhang:
As the developer during this sprint, I focused on the termination of Cloudinary and
found a workaround to store all the pictures in a local folder instead. I fixed all the
relevant code and made sure it deployed without issues. I was also responsible to finish up the packer
script I started last sprint. Now our testing environment can be deployed automatically. With a few adjustment
in the vagrant file, all you need to do is type vagrant up and the inline script would handle the rest.
---
## 7.Referenced Material
---
