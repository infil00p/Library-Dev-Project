# Library Dev Project

This is yet another proof of concept for Android Plugin Management for Cordova.  Currently, we
dump code directly into the platform's main project and there are a few problems with this
approach that we are noticing when we are working on non-trivial projects.

* Resources for the Plugin are intermingled with the Project resources
* Native UI had to be written programatically
* Dependency hell w.r.t. client libraries used by the third party dependencies

This approach uses the InAppBrowser and allows us to maintain the InAppBrowser as its own
project instead of a cancerous wart that gets tacked onto the side of an existing Cordova
application.  However, all plugins could be implemented this way.

Once again, this is a Proof of Concept and is not meant to go into any production code as is.
