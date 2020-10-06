# newsapp-file-uploader

# Overview

This application basically able to upload files to the Google Drive using Google OAuth2 validations. Also users can view their upload history using the dashboard that provided inside the application. 

## How to setup application

### Step 01 - Configure Google Services

As the first step you should enable the Google Drive API from your google cloud console api library and you must create OAuth Credintials from google cloud. For genarate Google OAuth credintials, you must provide following credintails,

- Application name
- Authorized Redirect URI `(For this application please provide http://localhost:5000/google/callback as the Authorized Redirect URI)`

Then you should give those genarated credintails into emplty feilds that provided inside the  `credentials.json` file such as,

- client_id ( `###############################.apps.googleusercontent.com`)
- client_secret (`#########################`)
- redirect_uris ( `http://localhost:5000/google/callback`)

### Step 02 - Configure Database

Setup your mongoDB database by giving URI of your mongoDB database that you going to use in 
`mongoose
  .connect("YOUR MONGODB URL", {
    useNewUrlParser: true,
    useUnifiedTopology: true,
  })`

### Step 03 - Node Module Installation

Use `npm install` to add all node modules that used for this application

### Step 04 - Run Application

Use `npm start` to trigger express server and run application. To view application you should go to `http://localhost:5000/` using prefered browser.


