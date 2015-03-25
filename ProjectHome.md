## Introduction ##

This is an attempt to write a JSR168 Portlet for managing users files on the server or a fileserver with the server network.

The Portlet works with all major browsers (Firefox, IE, Opera, Safari, Konqueror)

## Client and Server Requirements ##

**Client Requirements:** Any modern browser works (Firefox, Konqueror, Opera, Safari, IE6+) since all processing is done serverside. Client should support  HTML4+, Javascript1.5+ and CSS2+

**Server:**
  * JDK5+, any JSR168 portlet container (eg: Gridsphere 3.0.8 atleast, 3.1 works)
  * JSCH v0.1.37 atleast
  * Apache Ant 1.7.0
  * Familiarity with Java, Portlets
  * Apache Tomcat 5.5.25+
  * SSH2 / SFTP server on the fileserver.
  * SSH key based authentication

My Development and test env is Debian Linux and CentOS4/RHEL5.

I do not support Windows on the server side since I am not familiar with Windows Server. I am aware of issues with Win server (such as path delimiters hard coded to Unix style paths)

Please file a bug report if you observe anything wrong.

## STATUS ##
The code is still under heavy development and is expected to stablize around Sep-2008. Currently, the following features work:

  * Browsing home directory
  * Select and Delete files / dirs
  * View files (mime type : text only)
  * Navigate up
  * Files are sorted. Directories are grouped together and files are grouped together.
  * Zip files / dirs
  * Uncompress zip, tar: gzip or bzip2 files
  * Download files (needs some more fixes)
  * Portlet File Uploads
  * Completed - Copy/Cut & Paste file/dirs (v4.0.3)

## In Progress ##
  * Remove hard coded values (v4.0.3)
  * Security Audit

## TODO ##
  * Fallback to password auth if sshkeys are not setup
  * Test on Other Portal Servers : Sun PS, Pluto, jBoss etc
  * Security Audit, more input validation
  * Return error object instead of strings
  * I18N
  * Rename file/dir
  * Properly provide attributions
  * Many more ...

## License ##
The project is released under GNU GPL v3 license.

Some of the icons have been copied from my Linux machine and some icons from Ajaxplorer project (GPL2).

Regards
Anand Vaidya