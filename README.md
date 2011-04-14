BaseX Meta
==============

This is the one-size-fits-all metapackage to build various parts of the BaseX distribution.

It depends on the following projects:

* BaseX (the main project)
* BaseX Extended Tests (stress tests etc.)
* BaseX API (xqj etc.)
* BaseX Dist (distribution files)

Ideally, depending on your platform, `mvn package` does the following:

* Runs the extended test suite against your distribution
* Windows Installer / Executable
* Zip Archive
* Mac OS X Disk Image

Building
========
[Maven](http://maven.apache.org/ "Maven - 
    Welcome to Apache Maven") is required for building the project.

Please make sure you are familiar with the concept of [git submodules](http://book.git-scm.com/5_submodules.html "Git Book - Submodules") and [maven modules](http://sonatype.com/books/mvnref-book/reference/pom-relationships-sect-pom-best-practice.html#pom-relationships-sect-multi-vs-inherit "3.6.&nbsp;POM Best Practices | Sonatype")

In a nutshell issue the following commands to get started:

* `git clone git@github.com:BaseXdb/basex-meta.git`
* `cd basex-meta`
* `git submodule init` to initialize the remote repositories containing the actual projects
* `git submodule update` to actually clone these repositories


Maven Goals
__________

* `mvn test` to run the normal and extended BaseX Tests
* `mvn package` to run the package scripts for the basex & basex-api package. This leaves you with
** **basex** 
*** `jar` 
***  `exe` (where applicable) 
*** `App Bundle` or Disk Image (if mvn is called on OSX)
*** `.deb`


Feedback
========

For questions or feedback - both is very welcome - feel free to use the Tracker or our [Mailinglist](http://basex.org/open-source/ "BaseX | Open Source").

Thanks. 
