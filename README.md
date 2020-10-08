# Zoho mailboxes Migration to Microsoft Exchange 

Zoho configuration Prerequisites 


1. Deactivate the MFA (multifactor authentication from the administration console of Zoho)
https://www.zoho.com/es-xl/mail/help/adminconsole/two-factor-authentication.html

2. Enable the IMAP sign in option on every personal mailbox 
https://www.zoho.com/es-xl/mail/help/imap-access.html#EnableIMAP

3. Create the users and assign licenses from Microsft 365 (the password of the user must be equal to the Zoho Mail password, and we have to unable the M365 option that has to do with a chance of the password by the user when he enter to outlook)
https://docs.microsoft.com/en-us/microsoft-365/admin/add-users/add-users?view=o365-worldwide

4. The users must validate their M365 Account going trought aka.ms/outlook, they will see empty their mailboxes, but the should have access.

5.We should do the steps  from this next documentation:
https://docs.microsoft.com/en-us/exchange/mailbox-migration/migrating-imap-mailboxes/migrate-other-types-of-imap-mailboxes

5.1 Get the server endpoints from Zoho and configure them on M365 Exchange Admin centre
https://docs.microsoft.com/en-us/exchange/mailbox-migration/migrating-imap-mailboxes/migrate-other-types-of-imap-mailboxes#step-3-connect-microsoft-365-or-office-365-to-your-email-system
The values of Zoho are :
Servername          Port
imappro.zoho.com    993

smtp.zoho.com       465

5.2 Create a CSV file with thre columns with Excel, on the first column the "A" we write the M365 mail address, on the column "B" the Zoho Mail address, and in the column "C" the password that shoud be equal at Zoho and M365 service.
https://docs.microsoft.com/en-us/exchange/mailbox-migration/migrating-imap-mailboxes/migrate-other-types-of-imap-mailboxes#microsoft-exchange

5.3 Create a migration try, we should have all the previous described steps done.
https://docs.microsoft.com/en-us/exchange/mailbox-migration/migrating-imap-mailboxes/migrate-other-types-of-imap-mailboxes#step-4-create-a-migration-batch-and-migrate-your-mailboxes

5.4 The migration of the mailboxes can take several minutes or hours depending on the size of each one, you can see the progress an the M365 Exchange console-> users -> migration

6 After migration we strongly recommed to have a redirection of the Zoho mail to m365
https://www.zoho.com/es-xl/mail/help/email-forwarding.html#alink1



