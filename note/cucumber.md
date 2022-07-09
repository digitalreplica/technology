---
tags: a/note
---
in:: [[technology]]

# Notes
Cucumber is a plain-english software testing tool

## Howto

Running cucumber tests from command line
—
mvn test -Drunner=“com/user/testing/cucumber/runners/emberclient/EmberclientSecurityRunner1.class” -Dbrowser_config=“firefox_localhost” -Denvironment=“dev” -f functional-test/pom.xml -Dconsole.log.level=“OFF”
—

Security testing with cucumber
https://github.com/gauntlt/gauntlt
https://github.com/garethr/prodder
http://netsense.ch/download/pentestmag-may2012-behaviour-driven-security-testing.pdf
