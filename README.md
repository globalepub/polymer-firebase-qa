# Polymer + Firebase Q&A

A simple Q&A app built with Polymer and Firebase. Covers routing, authentication, material design, and CRUD operations.

- [Live Demo](http://polymer-qa.divshot.io/)
- [Video Walkthrough](https://www.youtube.com/watch?v=gErWcBdd-F8)

## Running Locally

Create a new app in Firebase. Set up a new GitHub application and [configure authentication](https://www.firebase.com/docs/web/guide/login/github.html) in Forge. Run the following command in your terminal:

    npm install && bower install

Edit `/app/elements/app.html` and change `<your-firebase>` to your Firebase URL:

```javascript
Polymer({
  ready: function() {
    this.globals.firebase = '<your-firebase>';
  },
```

Run the server locally with Grunt:

    grunt serve
    
##Firebase Hosting

You can run your new app under Firebase Hosting and check it with your firebase: https://your-firebase.firebaseapp.com/
Run the following command in the directory of your app downloaded.

###SETUP & INSTALLATION

- First Time Installation
You should have Node.js installed (you do not need to run Node, just have it installed)
```
    npm install -g firebase-tools` or sudo npm install -g firebase-tools
```
- Updating Previously Installed Firebase Tools
```
    npm update -g firebase-tools or sudo npm update -g firebase-tools
```     
- Edit `firebase.json` and change the file to:   
```
{
  "firebase": "<your-firebase>",
  "public": "app",
  "ignore": [
    "firebase.json",
    "**/.*",
    "**/node_modules/**"
  ]
}
```
The public setting tells the firebase command which directory to upload to Firebase Hosting.  

###DEPLOY YOUR APP
```
    cd <into your app directory> and run firebase init
```     
Then deploy your app with:
```
    firebase deploy
```
Now go back to your Firebase Dashboard online and then into Hosting, and click on https://your-firebase.firebaseapp.com to browse your app.
