## hindex.m ##
Computes the h-index of an author from Google Scholar.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/hindex.m)

```
%HINDEX  Computes the h-index of an author from Google Scholar.
%   HINDEX(AUTHORNAME) computes the h-index of the author AUTHORNAME, on
%   the basis of the publications referenced by Google Scholar
%   (http://scholar.google.com). An active internet connection is required.
%
%   The index h is defined as "the number of papers with citation number
%   higher or equal to h", and has been proposed by J.E. Hirsch to
%   "characterize the scientific output of a researcher" [Proc. Nat. Acad.
%   Sci. 46, 16569 (2005)]. Note that the number of citations referenced by
%   Google Scholar may be lower than the actual one (old publications are
%   not available online).
%
%   The string AUTHORNAME should contain the last name, or the initial(s)
%   of the first name(s) followed by the last name, of the author (eg,
%   'A. Einstein'). Do not put the initial(s) after the last name. The scan
%   is not case sensitive. Points (.) and spaces ( ) are not taken into
%   account. See Google Scholar Help for more details about the syntax.
%
%   Example: HINDEX('A. Einstein') returns 43 (ie: 43 papers by A. Einstein
%   have been cited at least 43 times, according to Google Scholar).
%
%   H = HINDEX(AUTHORNAME) only returns the h-index, without display.
%
%   HINDEX(AUTHORNAME, 'Property1',...) specifies the properties:
%     'verb'       also displays the list of papers returned by Google
%                  Scholar, rejecting the ones for which AUTHORNAME is not
%                  one of the authors.
%     'plot'       also plots the 'Cited by' number as a function of the
%                  paper rank.
%
%   HINDEX should be used with care. Many biases exist (homonyms, errors
%   from Google Scholar, old papers are not available online, but
%   unpublished or draft papers are...) For the true h-index of an author,
%   it is recommended to use an official citation index database (eg, ISI).
%   Use HINDEX just for fun.
%
%   Remark: Massive usage of hindex may be considered by the Google
%   Scholar server as a spam attack, and may invalidate the IP number of
%   your computer. If this happens, you get an 'Internet connection failed'
%   error message -- but you still can use Google Scholar from a web
%   browser.
%
%   F. Moisy, moisy@fast.u-psud.fr
%   Revision: 1.11,  Date: 10-jul-2006
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)