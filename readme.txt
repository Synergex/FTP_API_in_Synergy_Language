Name			FTP API in Synergy Language

Developed by            Chris Blundell, United Natural Foods

Contact                 Chris Blundell

Description             This is a set of routines that implement a basic
			FTP client in 100% Synergy code making use of the 
			Synergy Socket API.

Files included		ftp.dbl, ftp.def, testFTP.dbl, readme.txt

Platforms supported	Windows, OpenVMS, should work on UNIX but not tested

Minimum Synergy/DE version supported
			6.3.0

__________
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
