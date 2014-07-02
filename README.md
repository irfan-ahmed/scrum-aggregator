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

##License
* `scrum-aggregator`'s code in this repository uses the MIT license. See the `LICENSE` file.
* [AngularJS](http://angularjs.org) : <https://github.com/angular/angular.js/blob/master/LICENSE>
* [moment.js](http://momentjs.com/) : <https://github.com/moment/moment/blob/develop/LICENSE>
