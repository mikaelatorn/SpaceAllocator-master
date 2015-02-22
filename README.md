SpaceAllocator
==============

SpaceAllocator is a room booking system developed as a programming project in the SEM program at GU in the fall of 2014. See the file TODO.md for a list of what is planned. The TODO file also serves as a brief log of our sprints right now.


Running
==============
For the beta hand-in we now have a packaged file called SpaceAllocator.war which you can run on a web server that supports .war files. This is tested with Apache Tomcat 7. Put the war file in the directory preferred by your server software and start the server. In your web browser then go to http://localhost:8080/SpaceAllocator to interact with the application. Other server software may use different default ports than 8080.


User accounts
==============
<b>When using the sample data, you can log in using the following username/password combinations:</b>
  - student/student
  - lecturer/lecturer
  - admin/admin

...of which all users can make a reservation, but only admin can access other pages than the first one.


Beta hand-in notes
==============

  - The state of features: The admin can add rooms. All users can add reservations. There are currently no rules for which dates make sense in a reservation and there are no filters for which reservations or rooms are shown. Admin can clear lists of rooms and reservations.

  - This version does not use the translator from group 7, as you can see in the file RoomDao.java (in the spaceallocator.dao package) we have got some methods implemented by them however we need a complete translator package to switch to a database solution because our current implemented features use one table, which the current translator has no methods to interact with. Right now we are using some mockup objects that manipulate a class with six static lists in memory to hold the data. This means that the changes to the application content is lost when the application is shut down. <b>Hopefully it is obvious that it is transparent from our implementation point of view if we are calling the mockup DAO objects or the upcoming "real" DAO objects and how the data is stored. So we are not worried about not having database connectivity yet, especially since group 7 now has learned how to make one DAO class which means making the rest will be really simple.</b>


Reading
==============

To fully understand the components involved, you may want to read up on
  - Spring MVC (Currently we use the ObjectDB database system. At the ObjectDB website there is a good short tutorial on how to set up a running Spring MVC project powered by ObjectDB which was followed to have the basic file and directory structure for this project). Also read up on the MVC pattern in general. In short, when this application is compiled, it is packaged into a file that the web server can execute. The web server looks for servlets (defined in web.xml), it finds and executes the Spring MVC servlet. Spring then looks for it's context file (spring-servlet.xml). In that file we declare some options including that we want to use some annotations, where our .jsp files are stored and so on. In our java files, the @ annotation marks make Spring know which parts of our code are objects we want to store (models), which are controllers etc. The controllers all specify an address they want to bind to, for example you can say a controller should handle the "/rooms" address. They then implement the logic needed to calculate values we want to use, and then sends this to the view, which defines how things look. Views use JSP for the dynamic content.
  - JPA, Java Persistence API. This handles the details of the database and when using the ObjectDB implementation of JPA we don't have to manually create tables etc. Instead we create models (parts of the data model), by marking the data types (classes) we want to store with the right annotations, and from our perspective we can view it like data is stored and retrieved in the form of Java Objects. The database interaction is handled by a set of DAO (Data Access Object) classes. Some database queries will contain JPA Query Language (JPQL) which is very similar to SQL, most will just consist of telling the "Entity Manager" to store or merge changes to an object. The DAO classes will be written by group 7. 
  - GIT and using GIT from Eclipse (at least you found your way here. But reading up quickly on terms like branches, forks, push, pull, commit etc is probably a good idea if you're new to this, which we all are) 
  - Read a quick introduction to Maven if you feel like it.


Development
==============

This is an Eclipse Luna project where Maven handles dependencies (you don't have to use Eclipse if you don't want to, you can probably use Maven manually or use another IDE that can handle Maven. Using Eclipse is probably the easiest way though if you don't have any other preferences). Getting the EE package of Eclipse Luna may be a good idea, but you can always add plugins needed in Eclipse in "Help > Install new software". You will need Maven support (titled m2e under collaboration), and various packages under Web (Java EE, Java Web etc). Eclipse Web, Eclipse Javascript etc can also be nice to have.

Preferably use Tomcat as a Maven plugin to run the web application - just create a run/build configuration with these goals:
"clean org.apache.tomcat.maven:tomcat7-maven-plugin:run -e" and it will be fetched and run automatically. The first time you build it, Maven will also fetch all other dependencies needed, so until you do this, don't panic if Eclipse complains about errors in the code (unresolved dependencies). In your web browser then go to http://localhost:8080/SpaceAllocator to interact with the application.

To make a .war file, make a run/build configuration with these goals: "compile war:war". The .war file will be created in the "target" directory.

When not using an "organization" at GitHub, all collaborators has read/write access - develop in branches and do a pull request. We'll probably get a feeling for this after a while. Also generally commit only the files you have changed or added unless you know you have changed some overarching project settings (otherwise it may be your IDE that has changed some paths here and there in project files to get it to work on your particular setup and there is no reason to bounce these settings around), also the default setting in Eclipse seems to be that newly created files are not automatically included in commits (so you have to check the files in the commit dialog).
