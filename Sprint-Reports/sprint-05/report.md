## 1. Team members functions<br>
Maryam Ibad (Project Manager)<br>
Wenzhao Zhang (IT Operations)<br>
Akshay Patel (UI/UX Developer)<br>
Hugo Zamarripa Vazquez (Jr. Developer)<br>
Junhua Dong (Tom) (Developer)<br>
Jingwen Yu (Back up for all five roles)<br>
<hr>
## 2. Goals for this Sprint<br>
- Add 'confirm password' when signing up.
- Improve design layout for the All user page in admin.
- Preseed database with test users.
- Add 'next page' option to avoid endless scroll.
- Move more towards the functinality and usage features.
- Be able to upload more images at once.   
- Developed UI with background image and better visibility.
- Explore ways to add more features such as 'like/unlike' and location etc.
- Resize image size via css when uploaded.
<hr>
## 3. Accomplishments<br>
- Continue adding more functions into web application, our web now supports multi-tag functionality, multi-upload function, 
- We have a background image that represents the team.
- Admin user has the 'delete all' function.
- Improved 'all user' page.
- Redesigned admin user functionality >> delete all, edit, comment function. 
- Pre seeded test users.
- Added warning appearance when empty data detected.<br>
  ## next sprint goals:
  - Add 'next page' option when viewing images.
  - Add 'like/unlike' function.
  - Add confirm password when signing up.
  - Resize image being uploaded.
<hr>
## 4. Bug tracking<br>
- In our last sprint we encountered a bug where CSS was not being picked up in our newly added pages which is fixed now.
<hr>
## 5. Security Assumptions<br>
We have created a .gitignore file and have add all these security-related files in it, to avoid it being pushed to our repository. The SSL keys are now self-generated by our post-installation script for packer.
<hr>

## 6. Team members comment<br>
Each team members' comments on their accomplishments
- Akshay: As a UI/UX designer I focused on how the website looked and how smooth it was on different screens. We were still having trouble with that so still needed to be fixed. Then for UI I wanted to see and test how our product was laid out, and fix anything that was in the wrong layout, and reporting the problems with the project manager. Adding and updating pictures and colors to the whole website was a new task that i worked on this time. <br>
<<<<<<< HEAD
- Hugo:  As a junior developer two of my main tasks to get working where editing the metadata in the pictures to change the tag function, and to add multiple images while retaining a dynamic way for adding a tag to each image being added. I was unable to figure out the changing the meta data because it would not remove the old tag but add a new one alongside the old one. I hope to figure out how to fix this problem in the future<br>
- Jingwen: <br>
=======
- Hugo:  <br>
- Jingwen: I focused on implementing password confirmation field when users sign up. The passwords should be matching by using the express-validator module. Currently, the password confirmation is not fully implemented. <br>
>>>>>>> a23e993cd96be57e8495e39025890ce0e9d2dd8e
- Tom:  As a Developer, I fouces maintain the project code. In this sprint, I have modefyied the admin route function.<br>I have add the delete function of image and comment for admin so that admin can manage more easy for the image and comment.<br>
- Maryam: As a project Manager for this sprint, my main role was to assign the needed tasks to team members according to their role for this sprint, while managing all the task and coordinating with the team on the progress of the tasks. For this sprint my goal was to add more fucntionality to our web to make it look more like our target's (instagram) website and make it more user friendly. I assigned the task accordingly after viewing the functionality features of our target's web. <br>
- Wenzhao: As the IT operations, I constantly checked our newest version of the application are working in our Ubuntu 16.04 environment to ensure all bugs and issues are identified and solved. I pre-seeded our database with 15 test users with every password hashed. I also collaborated with Akshay to work with the layout design and the CSS side of the project. <br>
<hr>
## 7. Referenced material<br>

Data function build :
- https://github.com/aheckmann/gridfs-stream
- https://docs.mongodb.com/manual/reference/operator/query/in/?fbclid=IwAR2lLmGhybs77WMN20C_KSAqYdJICNMevqTdmbQ8bsnevecqlac0cR605DM
- https://flaviocopes.com/node-mongodb/
<hr>


o	Use case 1: Login as an already existing user (user’s information that was preseeded upon site creation)
o	Use Case 2: Execute the entire user story demonstrating all features you have coded (such as making a post, editing a post, and deleting and searching for a post)
o	Use Case 3: Login as an administrator or superuser and demonstrate and explain how the UI has changed.  Then demonstrate the administrator activities you have programed.


Each Project will have additional specific details per job to be delivered once project subject is determined and require you to explain your implementation and decisions in these categories: Each element here where applicable needs a git commit SHA and URL and or a Trello card

1.	Language and framework of your choice (ITM 311, ITM 312, ITMD 361, ITMD 411)
- We are using the node.js as environment language and express as the framework.<br>
<hr>
2.	Operating System Platform of Choice (ITM 301, ITMO 456)
- Ubuntu Vanilla 16.04 was used because of its has a relatively small installation size and all the dependencies / packages we needed for our projects are available on it.
- We are using a list of npm packages for our projects, includes: express, gridfs-stream, multer, passport-local
<hr>
3.	Use of Data Store/Storage (ITMD 421, ITMD 411, ITMO 456)
- We are using MongoDB for data storage, and Gridfs in cooperated to store images to our MongoDB, it divides our image files into small chunks of data which are then stored within the MongoDB collections.
<hr>
4.	Data encrypted at rest (ITMS 448)<br>
- All our user password are hashed and stored in our MongoDB user schema
- ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/hash.JPG)
<hr>
5.	Database makes use of master/slave replication (~ITMD 421, ITMD 411)<br>
- Schema creation: User Schema for user, and mongodb automatic generated metadata table for image(upload.files shcema and upload.chunks schema), all the comments are stored in the comment schema.
- ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/schemas.JPG)
- Master for database writes: MongoDB primary dataset will be used to write data. The primary dataset will perform all write operations and store user data.
- Slave for database reads: Data will be read from MongoDB replica set. The replica set will then replicate what’s in the primary dataset and serves as a backup. The master slave replication has been deprecated, so we use replica set to read from primary database.
<br>
<hr>
6.	Use of Responsive design (where applicable) (ITMD 361, ITMD 362)
- We use Bootstrap and also write our own CSS to overwrite some of those (With the !important rule). Bootstrap is used to create an overall design for our website, while CSS is used to adjust small details and customization.
<br>
- ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/responsive.PNG)
<hr>

7.	Use of https (ITMS 448, ITMO 456)
- Self-signed certifications are created in part of our post-installation script and we configured a .gitignore file to ignore it.
- All ports are blocked, only port 443 and 80 are explicitly allowed in Vanilla 16.04 since it is served as a web server.
- Records can be preseed via db.collection and the collection.insertOne method.
- https://flaviocopes.com/node-mongodb/<br>
<hr>
8.	Use of user authentication (ITMD 361)
- We use passport-local module for user authentication.

- The basic features for different types of users remain the same to our previous sprint:
- As unauthenticated users, they can view images uploaded by other users and search them based on tags.
- As authenticated users, they can do all the things unauthenticated users do, additionally, they can upload their images with or without tags to our Cloudinary storage, they can also edit or delete their own pictures.
- As administrative users, they have the same permission as authenticated users, additionally, they can take down any pictures that are inappropriate, regardless of the users that upload it (copyright violation,  - sensitive contents)
- UI is modified per authenticated user via CSS<br>
<hr>
9.	Creation of Dev Environment (local laptop), (ITMO 456)
- Packer script and vagrant is used to create an Ubuntu Vanilla 16.04, referencing Professor Jeremy’s given script with modification. Our web app is deployed in our dev environment automatically at start up by utilizing pm2, a node.js process manager. It is installed and set up via the post installation script.

- We asked some of our classmates to test our website again and provide us further feedback, hence we added an image of a hawk in the background to represent the team and make the website look nicer.

- Demonstration of bug reports being filed, tracked, fixed, and closed via Trello cards and GitHub commits
- Bugs are filed and tracked via Trello and GitHub issues
- For example, we had a bug that we weren’t be able to see the images when we are in the all pictures view, it was not picking up the path for the images due to deprecated URL. The bug is now fixed and has been moved to 'done'.<br>
<hr>
10.	Layout design (ITMD 361, 362, ITMM 471)
- Diagrams are located under Diagram -> UI -> UI_Diagram folder
- Current layout
- ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/UI/UI_Diagram/desktop_add1.png)

- We are still using the following resources to adjust our fonts and colors:
- We used this chart to adjust our font sizes in different view
- http://cristian.sulea.net/blog/css-font-size-px-vs-em-vs-percent-vs-pt/
- We used this to pick our color and generate RGB values
- https://www.w3schools.com/colors/colors_picker.asp

<br>
<hr>
11.	Management of Visio (or comparable) diagram tool of work flow (ITM 301, ITMO 456)
- Flowchart is under the folder Diagrams / UI
<br>
<hr>
12.	Management of project progress (ITMM 471)
- a.	Trello – correlate completed goals to DONE Trello cards and unfinished goals to in progress Trello cards
 - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/bugs-fixed.png)<br>
 - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/background-image.png)<br>
 - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/all-user.png)<br>
 - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/admin-user.png)<br>
 - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/pre-seed.png)<br>
 - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/warning-emptData.png)<br>
  - ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/multiple-upload.png)<br>

- b.	Slack - Slack is used for daily communications and notification of GitHub commit
- c.	Development Environment – What development environments were used by the team members? Node.js and atom/ vscode as code editor Ubuntu Vanilla 16.04 is our main dev & test environment.
- d.	GitHub - correlate completed goals to GitHub commits.
- Goal 1:
- GitHub commits SHA value:
 8d48fe4f1df668b44646c831fb5a62beb0cfcced <br>
- Goal 2:
 fbaf6231cf6a56c09d9d9a30cab9e91572f2081f <br>
 23f6215a336d66d3663776162ce9e6421dbdee10 <br>
 fe397261830e5789f3909944b2737ef89ee1b11a <br>
- Goal 3:
 621b0b2527da51e65af4d897f259873c4b2ed53a<br>
- Goal 4:
 2d7cfb508c0c7d82c49010256c28c76f1b644add <br>
- Goal 5:
 89f73ca1a2d198a4811e363b0eb97d1fd1de738d <br>
 d798a909c941ff7ef18f2a806c87202e54b8e1c9 <br>
- Goal 6:
 cbe9617c85ae0b6f0ff4f17148f9ca778a5d53d4 <br>
 
e.	GitHub Issues<br>
   Bug from last sprint fixed
- ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/bugs-fixed.png)
<br>
    Git commit SHA Value: d5baa75791c31ebbdb70533938a9b52db47fadaf

- Bugs are tracked via Trello, they are moved to the “Done” tab once they are solved.
<hr>
13.	Team must generate at least 15 real “test” user data that is inserted upon instance creation and proper data to test functionality of a system
- Test users are pre-seeded in our app.js file, we cannot insert them directly to the databases since it will fail the hash check. So we are calling the User.register method to register our users with hashes and they are being pushed to the database.
- ![Screenshot](https://github.com/illinoistech-itm/2019-team-08f/blob/master/diagrams/sprint-report-screenshots/test-users.png)
