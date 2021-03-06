scrum-aggregator
================
A scrum aggregator application that can collect and aggregate user scrum updates using nodejs and AngularJS

##Introduction
The scrum-aggregator application is a simple HTML5 application that shows a list of users that can provide updates for their work. The application view has 2 sections: Scrum section that records the scrum and a Users section where one can configure the users. There is also an 'All Scrums' page that lists all the scrums provided by a user. The application also uses the web browser's localStorage to keep record of the last user that provided the scrum.

The server is a node application that maintains the scrums and users in files and stores the scrums provided by the view. The node application is written as a cross domain application so that the view can be deployed on any web server and the node server would be running independent of the view.
  
##Features
1. Scrum: The page shows a form with list of users and an option to specify the scrum update.
2. Users: The page shows the list of configured users. One can add/modify a user from this page.
3. All Scrums: The page showing all submitted scrums.

##Quick Start
### The Server
####Configuration
The server is configured using a file called `config.json`. The file is located in at `server/config.json`. This file is used to provide data such as `port` and so on. The following table shows a list of parameters:

|Name|Information|
|-------------|-------------------------|
|port| The port at which the scrum application runs. Default 15080|
|scrumMaster|EMail of the person sending the scrum updates and reminders. Required|
|scrumAlias|EMail of the person/group/alias where the received scrum updates are to be sent. Required|
|serveStatic|A boolean to indicate whether the server also serves static content. If this is set to `true`, then the application view does not need to be deployed to any web server.|

Start the server application using node. The default port that the application runs on is set to `15080`. You can change the port in the `server/config.json` file.

```
$ node <application-dir>/server/scrumServer.js
```

###The View
Update `public/js/services.js` file and set URL with the correct `host` and `port` for the server in the `adminService` factory function. This should point to the node server application started above.

The `public` directory contains all the code for the view/docroot of the application. You can copy this directory as the `context-root` on a web server liver Apache or nginx. You can also create a softlink to the `public` folder if softlinks are supported on your web server.

##License
* `scrum-aggregator`'s code in this repository uses the MIT license. See the `LICENSE` file.
* [AngularJS](http://angularjs.org) : <https://github.com/angular/angular.js/blob/master/LICENSE>
* [moment.js](http://momentjs.com/) : <https://github.com/moment/moment/blob/develop/LICENSE>
