## Lets get something straight

I'm really not a fan of Java. But it has its place in the world running the user interfaces for really nasty network switches and as an applet plugin allowing extensability of the web into the desktop.

This means that as much as I'd love to drop it from our network managed Apple iMacs and Macbooks, I really cannot afford to.

## What's the problem?

Install once and be done with it. That is what I would like to be able to do when deploying a new mac onto the network. Unfortunately updates to Java occur and we do need to keep it updated as frequently as we can.

Internally we run updates such as these via Munki and once a new install of Java has been pushed to Munki. These updates run at our own schedule and the super annoying warnings that Java pops up we needed to supress until the next run for fear of worrying the users.

Additional security features have been added in recent updates which now either break or upset applets where the user keeps having to accept the applet.

## You did whuuut?

We supressed both of these sets of warnings by altering the deployment properties for the system install of java.

There is documentation here: 

[http://docs.oracle.com/javase/7/docs/technotes/guides/deployment/deployment-guide/properties.html](http://docs.oracle.com/javase/7/docs/technotes/guides/deployment/deployment-guide/properties.html)

For OSX this file is packaged into a .pkg and then deployed onto the macs using Munki.
