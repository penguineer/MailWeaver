MailWeaver
==========

Forward an e-mail to a mailing list and proxy responses to the sender if (s)he is not a member of this list


Scenario 
--------

The $hackerspace has a discussion list at list@$domain and a contact addresss at $kontakt@$domain. 

An outside party who is not a member on the list sends an e-mail to kontakt@$domain.

MailWeaver receives this e-mail and puts it on a curation list. All curators, i.e. those who would normally receive kontakt@$domain are informed about the new message. They have three choices:
a) Ignore the e-mail or mark it as spam.
b) Simply forward the e-mail, regaining the e-mail forward functionality.
c) Forward the e-mail to list@$domain as if it was originally sent there.

Option c) is the most interesting:
The e-mail is now posted on the mailing list. In case of an answer, which would go to the list, MailWeaver forwards the response to the original sender, allowing him/her to take part in the mailing list discussion.

Forwarding is transparently done based on the message-threading mechanism and only applies to a specific discussion.

As a result, an outside party can discuss just one issue on the list without taking part in _all_ traffic on that list.Forwarding  e-mails to the generic towards the list and relaying replies is no longer a manual task and the outside party will take part in the whole discussion.


Technology
----------

* backend uses Java with [JavaMail](https://javamail.java.net/)
* data is stored in an SQL DBMS (nothing fancy to be done here)
* contemporary HTML frontend
* attached to [mailman](http://www.gnu.org/software/mailman/)?

These are just the corner stones, this part needes to be refined!