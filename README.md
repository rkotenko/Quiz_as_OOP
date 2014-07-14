Simple_Javascript_Quiz
======================

This iteration has been converted to use objects.  The major navigation is done via the Quiz object.  Questions are objects as well as are Users.  However, the users are really just a skeleton.  I was going to extend here to store quiz answers via ajax calls to files, but will instead be doing that in other versions.

Also implemented here was Qunit testing.  I used it for unit testing of my objects and for interaction testing. It was a crash course really as I learned how to massage Qunit to test user interaction.  Each test resets its data and state back to whatever is in setup.  By saving that state to a global variable using jquery's detach(), I could inject that state back into the next test.  Thus, I could test the flow of the quiz from each state to the next without having to manually create the conditions of each one (which could result in a lot of developer error if I forgot to set a condition).  In this way, I could have a series of dependent tests which is good for interaction testing instead of the normal atomic ones.   

This is my first foray into javascript testing so there might be a better method of testing user interactions out there, but saving the state helps do a pretty decent job.

Also a pain were the async functionality I had in the code.  load() and fadeIn() required that I set my timeouts at a decent number so they could finish.
