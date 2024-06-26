# The Beginning

Creating the tenant was surprisingly straightforward. I simply signed up for a new Microsoft account, filled out some details, provided my credit card information, and even started out with a free month from the trial Microsoft offers. After setting up my tenant, the first order of business was registering a domain.

A quick Google search led me to Namecheap.com. A mere $6 later, I am now the proud owner of the domain `enamoradotech.com`!

# Fun with DNS

After purchasing the domain, I needed to add it to my Microsoft 365 tenant. While I was familiar with the theory behind DNS, I had never really worked with it hands-on. I knew about DNS records, but I had never had to configure them... This was a fantastic opportunity to learn more and solidify the knowledge I had gained when studying for my Network+ certification.

Following this Microsoft Learn document, I was able to set up all the required DNS records within Namecheap. I set up 7 CNAME records, 2 SRV records for Teams, 2 TXT records, and finally 1 MX record.

After a successful setup of all the DNS records, we are now able to send emails. The very first email was sent to our Director of Engineering, Amy!

![screenshot of first email.](https://github.com/derinp/EnamoradoTech/blob/main/images/firstemail.png)
