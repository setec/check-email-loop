### Welcome to the `check_email_loop` plugin repository
This script sends mails with a specific id in the subject via an given SMTP
server to a given email-adress. When the script is running again, it checks for the
delivery of this email based on its unique id in the subject on given POP3/IMAP
mail accounts. 

Using an external mail forward this script enables you to assert basic
functionality of sending & receiving emails of your email infrastructure.

Example
```
check_email_loop -poph=host -pa=pw -popu=popts -smtph=host \
     -from=root\@me.com -to=remailer\@testxy.com \ 
     -lostc=0 -pendc=2
```

DEPENDENCY INSTALLATION
This perl-based nagios plugins requires the perl IMAP and/or POP3 client module. 
Debian / Ubuntu users can install those dependency using
```
sudo apt-get install libmail-pop3client-perl libmail-imapclient-perl
```

### Note
This is a plugin I wrote centuries ago. Meanwhile I do not run any email servers
any more, but this plugin still seems to be very useful for a resonable share of
the nagios users so that many other supplied significant improvements and
extensions to this plugin. I'm very happy that my little script has become part
of this lively open source community.

Though I wont' be able to further maintain this plugin on my own, I'm still
trying my best to integrate code contributions I receive via email and share
them at this place. So if you have a litte code change correction you feel it
should find it's way into the public: just fork the GitHub repository and give
me a short note.

Please also check the user comments on this plugin as they might contain more
current information.
