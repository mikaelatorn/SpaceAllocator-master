Sprint 1
==============

Basic Spring MVC project running
Split packages into spaceallocator.model, spaceallocator.controller, spaceallocator.dao
Add models for room types and relation to rooms
Add other models...
Add spring MVC "web security" login mechanism

<b>How, why, etc:</b> Some of us had prior knowledge with PHP and knew this could be used to get a solution
with maybe less hassle than Java and Spring MVC, but wanted to learn something new. So the first week was mostly
playing around with this and getting to know Spring MVC, ObjectDb, jsp, Git and so on.


Sprint 2 
==============

(Stephen was focusing on translator for group 8)
Username should be automatic when booking
Room type should be selected from dropdown box
Reservations should have some kind of date/time
More sample data that makes sense
Move SecurityConfig to another package among with PasswordHash and other such settings (jerker)
Clean up code, add comments (jerker)
GUI improvement, perhaps add any CSS boilerplate/framework (mikalea and hari)
Expand directory structure for images and related resources similar to how the style folder works right now
Display error messages on failed login attempts


<b>How, why, etc:</b> We wanted to get some relationships between tables to be reflected in the UI so that's why we for example
wanted the rooms to be chosen from a dropdown box when adding reservation. A simple method to add sample data can be useful.


Sprint 3 (Starting wednesday November 19)
==============

No major changes, feature freeze before beta hand in!
Consider switching to the partly finished translator from group 7 we will receive this week (not doing it)
Look at how to run the compiled .war file on a server like tomcat
Mostly focus on packaging this for hand-in and presentation


<b>How, why, etc:</b> Before the beta hand-in we didn't make a lot of big changes, just made sure it worked
and cleaned up the code a bit. We learned that Maven is a really useful tool, it was very obvious when we tried to
create a .war file and needed to get all dependencies included and all the files to be put into the right directory structure
within the .war.


Sprint 3 (Starting wednesday November 19)
==============

Add "RoomType" controller and view similar to the room list right now (will be seen by admin only) (marcus)
Logic for checking whether reservation start/end dates are reasonable (not spanning different dates etc) (jerker)
Also consider "length" field in reservations instead of end date/time (not doing it)
Update object/relationships chart to reflect any such changes since they were first created
Conceptual ideas for GUI can be discussed
General GUI improvemenet (hari, mikaela)
Add Config controller and view, seen by admin only (jerker)
Update controller method and forms for editing rooms
Add "AccessLevel" controller and view similar to the room list right now (will be seen by admin only) (stephen)
Logic for checking for booking collision. Preferably one reservation can end in the same minute as another starts.
Only allow whole hours when choosing start time for reservations. Make a dropdown box or similar.

<b>Reflections, how, why, etc: </b> Marcus realized the magic of Spring MVC. The GUI design needs improvement before things make sense, right now it gets really visually messy when we add new features.
