# Hospital-API
We’re going to design an API using Node.js and MongoDB for the doctors of a Hospital which has been allocated by the govt for testing and quarantine + well being of COVID-19 patients

## How to set it up on your local Computer?
1) Clone the Package to your local System
2) Navigate to the folder wherein the project has been cloned
3) Open Terminal and type `npm install` [Make sure node is already installed in your system!]
4) Type `nodemon index.js` or `npm start` [Make sure mongodb is installed in your system ]
5) The app should run on default port 8000 or if you've mentioned env port it'll run on that.
6) Not working? Ping me!.

## What are the Different API's in this project?
1)`/doctors/register` → Registers a new Doctor to the hospital Database takes in madatory `username` ,`password` , and `name` of the doctor.\
2) `/doctors/login` → Doctor Login with username and password, if Authenticated, Returns the JSON Web token, takes in madatory `username` and `password`.\
3) `/patients/register` → API to register a new Patient, This is a protected route only authorized doctor can create a new Patient. Takes in madatory patients id, whichis the phone number as `phone`  and `name` of the patient.\
4) `/patients/:id/create_report` → API to create a report for the Patient with ID `id` . Takes in a mandatory field `Status` in it.\
5) `/patients/:id/all_reports` → To Show all the reports of a particular Patient with id `id`. unprotected Route.\
6) `/reports/:status`  → To Show all the reports in the database with a particular `status` lets say Positive or Negative Or Quarantined etc.\


## What's in the folders?  
1) Entry point : index.js
2) `config` : Contains configuration files of Mongoose and Passport Authentication Strategies. 
3) `Controllers` : The controllers for various API's or controller like Doctor or Patient  or Report controller.
4) `Models` : Mongoose Models for the Doctors, Patients and reports!
5) `routes` : index.js which manages routes efficiently to have a scalable project.
