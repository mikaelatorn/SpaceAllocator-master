TODO list
==============

Sprint 1

  - <s>Basic Spring MVC project running</s>
  - <s>Split packages into spaceallocator.model, spaceallocator.controller, spaceallocator.dao</s>
  - <s>Add models for room types and relation to rooms</s>
  - <s>Add other models...</s>
  - <s>Add spring MVC "web security" login mechanism</s>

Sprint 2 (Stephen is focusing on translator for group 8)
 
  - <s>Username should be automatic when booking</s>
  - <s>Room type should be selected from dropdown box</s>
  - <s>Reservations should have some kind of date/time</s>
  - <s>More sample data that makes sense</s>
  - <s>Move SecurityConfig to another package among with PasswordHash and other such settings (jerker)</s>
  - <s>Clean up code, add comments (jerker)</s>
  - <s>GUI improvement, perhaps add any CSS boilerplate/framework (mikalea and hari)</s>
  - <s>Expand directory structure for images and related resources similar to how the style folder works right now</s>
  - <s>Display error messages on failed login attempts</s>
  
Sprint 3 (Starting wednesday November 19)

  - <s>No major changes, feature freeze before beta hand in!</s>
  - <s>Consider switching to the partly finished translator from group 7 we will receive this week</s> (not doing it)
  - <s>Look at how to run the compiled .war file on a server like tomcat</s>
  - <s>Mostly focus on packaging this for hand-in and presentation</s>

Sprint 4 (After presentation, two weeks)
  - <s>Add "RoomType" controller and view similar to the room list right now (will be seen by admin only) (marcus)</s>
  - <s>Logic for checking whether reservation start/end dates are reasonable (not spanning different dates etc) (jerker)</s>
  - <s>Also consider "length" field in reservations instead of end date/time (not doing it)</s>
  - Update object/relationships chart to reflect any such changes since they were first created
  - <s>Conceptual ideas for GUI can be discussed</s>
  - <s>General GUI improvemenet (hari, mikaela)</s>
  - <s>Add Config controller and view, seen by admin only (jerker)</s>
  - <s>Update controller method and forms for editing rooms</s>
  - <s>Add "AccessLevel" controller and view similar to the room list right now (will be seen by admin only) (stephen)</s>
  - <s>Logic for checking for booking collision. Preferably one reservation can end in the same minute as another starts.</s>
  - <s>Only allow whole hours when choosing start time for reservations. Make a dropdown box or similar.</s>
 
Sprint 5 (Starting Dec 10)
  - Add Access Level selection to Room Type page and add update form (marcus)
  - General GUI improvemenet (hari, mikaela)
  - Keep working on "AccessLevel" controller and view similar to the room list right now (will be seen by admin only) (stephen)
  - Page separations of all lists (jerker)
  - Improve date selection for reservation (jerker)
  
Future
  
  - Receive fully working translator classes and switch to using them
  - Confirm question before delete or clear table
  - Delete button beside update option in lists
  - Add "User" controller and view similar to the room list right now (will be seen by admin only) (marcus)
  - "/update" controller methods and update forms in all views
  - Sorting methods for some lists
  - Consider writing simple unit tests (assert or similar) for translators for use during development
  - Consider methods/beans for common visual components such as text input fields
  - Error checking + on bad input in forms, show nice error messages and where possible the input the user entered should be displayed again in the form inputs
  - Improve rendering of reservations/schedule (hari and mikaela)
  - Schedule views: methods for rendering 1 day - 1 room, which we can use in combination to create a weekly schedule or show todays schedule for all rooms (or all rooms of a certain type)
  - Javadoc comments on nearly all methods, and comments in all XML files
  - Improve indentation and comments in JSP files
  - AJAX schedule browsing (optional)
  - Blueprint sketches of room (optional)
