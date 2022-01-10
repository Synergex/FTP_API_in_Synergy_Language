# FTP_API_in_Synergy_Language<br />
**Created Date:** 3/23/2007<br />
**Last Updated:** 5/20/2008<br />
**Description:** This is a set of routines that implement a basic FTP client in 100% Synergy code making use of the Synergy Socket API.<br />
**Platforms:** Windows; Unix; OpenVMS<br />
**Products:** Synergy DBL<br />
**Minimum Version:** 9.1<br />
**Author:** Chris Blundell
<hr>

**Additional Information:**
Discussion

I've seen some inqueries lately on the Synergy-L inquiring about FTP functionality
most of the answer have involved scripting in one form or another. Personally I'm
a control freak and therfore wrote an FTP client that could be used directly from
Synergy code. And allow the developer to maintain control of the connection.

Usage

All of the routines are contained in the file ftp.dbl but there are a small number of
macros defined for FTP functions that do not require special code to handle them.

The API can handle long directory lists and short directory lists, and it can handle binary and
ascii transfers (either put or get).

All of the routines pass back a result code which is the result code genrated by the FTP
server, or in the case of the initial connection a sockket error code.

The message text for a request is also passed back from the server in an optional message
parameter.
