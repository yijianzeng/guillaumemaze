## tweet.m ##
Send tweets !

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/tweet.m)

```
% tweet Send tweets !
%
% [] = tweet(MESSAGE,[PROP,VAL]);
% 
% Send tweets using the system command 'ttytter'.
% 
% Inputs:
% 	MESSAGE: A string with the tweet.
% 	PROP:
% 		- 'to': Send a direct message to VAL
% 		- 'id': Define the account to use to send the tweet.
% 				In this case, VAL is such that the keyfile ttytter will use
% 				is here: ~.ttytterkeyVAL.
% 				Type: ls ~/.ttytterkey* to see what's available
%
% Eg:
% 	tweet('Hello world !');
% 	tweet('Check this out ! http://code.google.com/p/guillaumemaze/source/browse/trunk/matlab/codes/inout/tweet.m A tweet from #matlab','to','MATLAB')
%
% Info:
% 'ttytter' is a perl code to use twitter from script and command line. Check it out at:
% 	http://www.floodgap.com/software/ttytter
% 
% Created: 2012-12-20.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)