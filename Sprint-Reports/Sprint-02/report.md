## 1. Team members functions
Akshay Patel (IT Operations)
Hugo Zamarripa Vazquez (Developer)
Jingwen Yu (UI/UX Developer)
Junhua Dong (Tom) (Jr. Developer)
Maryam Ibad (UI / UX Developer)
Wenzhao Zhang (Project Manager)
## 2. Goals for this Sprint
Complete the login / signup function on our site, integrate Cloudinary API to upload images with tags and retrieve them based on tags, redesign Multiview layout based on our current design, redesign flowchart to match our current process.
a. Although we were stuck on the retrieving function, we managed to solve it and accomplish all our initial goals.
b. For our future goals, we might have to consider the additional time to fix bugs and configure stuffs out when we identify our goals. During this sprint, we stuck on one goal and almost couldn’t fulfill it during this sprint.
## 3. Accomplishments/next sprint goals
a. We were successful in accomplishing our initial tasks, we made the login/ signup on our website functional, we completed the upload / retrieve images based on tags functions. We redesigned the flowchart as well as multi-view layout.
b. Our next sprint goals includes: Deploy automating system via packer and vagrant, refine our current site for midterm demonstration.
## 4. Bug tracking
Ubuntu Xenial 16.04 was used as our Dev & Test environment to test our program and resolve any bug issues. During Sprint-2 the most common bugs we found is on page redirections due to errors made during coding. We used Trello to track our bugs and update the status accordingly to avoid confusion among group members.
## 5. Security Assumptions
Relying on database security solely isn’t enough to create a safe enviorment. xxxxxxxx
## 6. Team members comment
Each team members' comments on their accomplishments
Akshay: "As a IT Operations, i was looking over the day-to-day activities and monitoring Website stability and performance. Both to directly supporting developer and to assist with the project. Making sure that we follow a certain procedures to ensure the IT Operations are working correctly."
Hugo: I worked with Tom to develop a search with tags, we solved this by doing a lot of deep reasearch into the cloudinary API documents to find we needed to match the metadata ID for each image and match it with the id of the metadata from the cloudinary image. We hope to do better next sprint in terms of communication and more early research. More steady commits between each other. We hope to able to do multiple search by tags. for example searching for photos with tags Cats & Dogs  
Jingwen: "As a UI/UX developer, I updated the layout prototype for each page and updated the flowchart based on our current state. I start working on the coding part of the layout."
Tom:
Maryam: "Being a UI/UX developer for this sprint, I helped the team with updating the layout of our project to meet our goals for the layout, and the flowchart."
## 7. Referenced material
https://cloudinary.com/documentation/admin_api
We used the reference page for configuring Cloudinary API.
https://github.com/jhajek/packer-vagrant-build-scripts/
We used Jeremy’s packer / vagrant repository as a reference to learn how to build an automated script.



# Project Base Requirements
## 1. Language and framework of your choice
Express(ejs) is used as the web application framework
Node.js(JavaScript) is used as our language
## 2. Operating System Platform of Choice
Develop using Visual Studio Code / Atom
Test on Microsoft Windows 10 & Ubuntu Xenial 16.04
Dependencies:
Multer: Handle form-data for uploading files
Passport: Handle authentication requests
Dotenv: Handle environment variables
## 3. Use of Data Store/Storage
MongoDB is used since we are not handling complex transaction and it is rather easy to implement.
## 4. Data encrypted at rest
MongoDB offers native symmetric encryption (AES-256-CBC) support
## 5. Database makes use of master/slave replication
Both Master / Slave instance can be initialized in MongoDB, since we are running with authorization enabled, we will configure a keyFile so that slave mongod instances can authenticate and communicate with the master mongod instance.
## 6. Use of Responsive design
We have multi-view design for phone, tablet and PC (via @media screen)
## 7. Use of https
We haven’t given much thoughts to this, but we will be using self-signing certificates for validation. A more detailed description will be provided in future sprint
## 8. Use of user authentication
As unauthenticated users, they can view images uploaded by other users and search them based on tags.
As authenticated users, they can do all the things unauthenticated users do, additionally, they can upload their images with or without tags to our Cloudinary storage, they can also edit or delete their own pictures.
As administrative users, they have the same permission as authenticated users, additionally, they can take down any pictures that are inappropriate, regardless of the users that upload it (copyright violation, sensitive contents)
## 9. Creation of Dev Environment
We will use given scripts as reference to build and pre-deploy our testing environment. This is our main goal for Sprint 3.
## 10. Layout design
We used lucidchart for project layout design to display the current project state.
## 11. Management of Visio
The use of Visio is to update the project flowchart from both the users and developers perspective. It helps us to see our workflow and make adjustments based on the flowchart.
## 12. Management of project progress
Trello, Slack, GitHub and WhatsApp is used for our communication and file sharing.
## 13. 15 real “test” user
Test users will be created via script during the creation of our dev environment.
