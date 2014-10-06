The Past, Present, and Future of CGI.pm

[Lee Johnson](http://leejo.github.io)

~~September~~ October 2014

---
## The Past

---
## The Past

Not interested in the past!

---
## The Past

OK, i *am* interested in the past but this is a lightning talk.

No time for that.

---
## The Recent Past

---
## The Recent Past

Mid 2013

* [p5p - RFC: Removing CGI.pm from the core distribution](http://www.nntp.perl.org/group/perl.perl5.porters/2013/05/msg202130.html)
* [chromatic - Ejecting CGI.pm From the Perl Core](http://www.modernperlbooks.com/mt/2013/05/ejecting-cgipm-from-the-perl-core.html)
* [perlmonks - Remove CGI.pm from Perl Core?](http://www.perlmonks.org/?node_id=1035434)

---
## The Recent Past

Mid 2014

* [The very first commit to perl 5.21](http://perl5.git.perl.org/perl.git/commitdiff/e9fa5a80) - CGI.pm is no longer in core
	* So as of perl 5.22 (mid 2015) perl will no longer ship with CGI.pm
* [CGI.pm needs new primary maintainer](http://www.nntp.perl.org/group/perl.perl5.porters/2014/02/msg212800.html) - Lincoln Stein
	* Which is [me](https://metacpan.org/release/CGI)

---
## The Present

---
## The Present

We know CGI (and by association CGI.pm) is still in use, in some cases significantly so. See those links 3 slides back.

---
## The Present

We know CGI.pm is still in use, in some cases significantly so.

* super search [perlmonks](http://www.perlmonks.org/?node=Super%20Search) for CGI - lots of results
* [stackoverflow](http://stackoverflow.com/search?tab=newest&q=perl%20CGI) lots of questions
* [jobs.perl.org](http://jobs.perl.org/search?q=CGI&location=) jobs matching "CGI"
* steady stream of issues raised - 1 or 2 a month.
* just take a look at [bugzilla](http://www.bugzilla.org/installation-list/)

---
## The Present

Version 4.* (2014 and beyond) backwards compatible.

* [Addressing issues](https://github.com/leejo/CGI.pm/issues?direction=desc&sort=created&state=open) - v4.* of
CGI.pm will address all open issues and any that are raised between now and v5
	+ RT Issues queue down to less than 10 from > 80
	+ 3/3/3 split in terms of already fixed/fixed/rejected

* [CGI::Alternatives](https://metacpan.org/pod/CGI::Alternatives) - a little documentation to point users of
CGI.pm at alternatives (sort of like Task::Kensho).

* Increasing test coverage.

---
## The Present

We know some perl developers still advocate the use of CGI.pm

---
## The Present

We know some perl developers still advocate the use of CGI.pm

* linkedin groups - walled garden, you'll just have to believe me
* much history on the web - search for perl + CGI
* books - search amazon.com for perl + cgi
* [a recent talk advocating CGI.pm](https://www.youtube.com/watch?v=0SfAoLNcvsk)

---
## The Present

We know some perl developers still advocate the use of CGI.pm

* linkedin groups - walled garden, you'll just have to believe me
* much history on the web - search for perl + CGI
* books - search amazon.com for perl + cgi
* [a recent talk advocating CGI.pm](https://www.youtube.com/watch?v=0SfAoLNcvsk). At mojoconf 2014!

---
## The Present

On that last link.

![not sure if serious](/img/serious.jpg)

---
## The Present

[Please stop!](https://www.youtube.com/watch?v=E1k6hT-cwJk)

---
## The Future

---
## The Future

Version 5.* (2016 and beyond?)

---
## The Future

Version 5.* (2016 and beyond?)

* Refactoring - replacing the pre-re-invented wheels
	* ~~package Fh - IO::*?~~
	* ~~package CGITempFile - File::Temp?~~
		+ Already done in v4 (many bugs in CGITempFile)
	* General stuff - URI::*?
	* multipart stuff - MIME::*?

---
## The Future

Version 5.* (2016 and beyond?)

* Removing - EBCDIC support
	* when this happens in perl it will happen in CGI.pm

* Removing - cgi-lib.pl compatibility
	* because cgi-lib.pl
	* it's only half compatible anyway

---
## The Future

Version 5.* (2016 and beyond?)

* Deprecating - mod_perl 1.* compatibility
	* possibly controversial
	* messy, and has no test coverage
	* mod_perl 2.* compatibility will remain

---
## The Future

Version 5.* (2016 and beyond?)

* Deprecating - *ALL* HTML generation functions
	* possibly really controversial
	* huge maintenance burden (50% of CGI.pm)
		* shouldn't be used anyway
		* replace docs with TT examples
	* soft deprecation - move into own package
		* clear notice that these are deprecated
		* PLEASE DON'T USE THESE FUNCTIONS!
		* warnings if used without $YES_I_WANT_TO_DO_THIS

---
## Thank you
