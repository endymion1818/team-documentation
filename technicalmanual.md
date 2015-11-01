

# Digital Development Technical Manual 
### Contributors: 	Ben Read
### Date: 			24 July 2015
### Location:		
### Version: 		0.4

---
## How We Fit In

##### 1. To the Company
Please fill in
##### 2. History
Please fill in
##### 3. Where we are Now

##### 4. The Future
Requirements for websites will grow. Client expectations will continue to mature as the web matures. We must deliver to client expectations even when these expectations are not explicitly known to us.
##### 5. To our Clients
The Web Development team
There is a web development team. You are the on site representative of that team. Other developers are contracted as required. You will probably be involved in assisting them. We will cover this later.
It must never become apparent to our clients that we are using an external contractor unless it is explicitly stated by the MD or an account manager.
#### Communication Standards
Communicating with clients must always be done in conjunction with the account manager. It must be considered carefully, be polite, and done in a professional manner.
Ensure that all information to and from clients is recorded for later reference.
All Emails to and from the client must be stored in the appropriate job wallet.

#### Company Processes
Please fill in
### The Account Management Process
Please fill in
### Initialisation
A new project is identified. A new job wallet is opened in the client documentation folder.
The account manager will generate a job number. This job number can be used to tie in all designs, project management and client communications. Use it.
### Liaison
Normally, requirements will come from the account manager individually or during meetings. It is your job to understand these requirements so that the account manager can liaise with the client effectively.
Try to analyse how the project requirements can be met technically, even if you’re not compiling the scope.
Throughout the project, notify the account manager of any delays or possible issues that you may encounter. The account manager sets the budget for the project so needs to keep a close watch on how much it’s costing. Your time is part of that budget.
### Completion
Projects should be completed on a testing server.
Hosting on our development server avoids some potential problems:

- Potential theft of work
- Compromising the clients live site or server
- Allowing us to control how much the client sees and when

Work should be moved to the live domain only after testing, client approval and final billing.

### Contractors
Other (offsite) developers are contracted as required. You will probably be involved in assisting offsite contractors in 2 ways:

#### Support
Offsite contractors may need access to servers via control panel, FTP or SSH. It is up to you to ensure they receive these details.

For new contractors, please ensure you restrict their access. For example, don’t give them root access to a server, or Administrator access to a CMS unless it is absolutely necessary.
#### Management
You may be required to manage their workloads for larger projects or where the brief is to do major work.

You will have to choose the best tool for doing this, but I have had great success using Trello (http://trello.com/) because it gives CONTEXT.

_Context is important because it helps developers anticipate what you might be talking about. You will find that when you have contextual communication, it is much easier to obtain the communication that you need from other developers._

It is strongly recommended that you become involved whenever contractors are called in so you can parachute in as required. It also helps to know if changes are being made to a website so that if an issue is revealed it’s source can potentially be identified more easily.

Although you may be responsible for day-to-day management of contractors, ultimate responsibility and decisions belong to the MD.

---

## Building a New Site

### The Waterfall
Blaze operates on a ‘waterfall’ process. That means when a new site comes in, it goes from the account manager to you for scoping. Once the scope has been created it goes back to the account manager for approval. Once approved, the account manager sends it for design.
Once the design has been signed off by the client, the account manager will give approval to begin the build.
You will probably not have any text content or images at this stage. Don’t let that stop you.
Please review the embedded document for an idea of the waterfall process we follow:

### Scoping
The project should be scoped by you and the account manager. The scoping process sets down what functionality will be build based on the project requirements.
I have produced a Project Scope template to help catalogue and describe the scope in an Agile format. The template is kept in -FOLDER-

### Key Deliverables
Some clients have key goals for their websites. As our clients become more used to the way the internet works this will become more useful. Key deliverables could include performance goals, conversion rates or SEO objectives.

### Build Specifications
This outlines some basic principles for the construction of the website. It is especially important that clients understand that building a website that is functional in IE8 or Android 4.0 and older is an extra cost that is chargeable.

### User Stories
I have used the format of user stories because it helps developers to understand not only the goal of the user but also their intention. This can be important in helping you decide whether there is a better, simpler or more cost effective way to implement the scope.

### Site Map
A Site Map enables us to scope which pages appear in a project, and may also cover which pages appear in the navigation areas. The Site Map is a client deliverable which the client will be signed off prior to build.
You can find the site map in -FOLDER-

### Design
Although developers do not typically get too involved in the design phase, it is important to be on hand to respond to questions from designers. As our designers are not always aware how their decisions will affect the build, it is up to you to challenge the design tactfully and kindly when there is a potential problem—preferably before the design is seen by the client.
This opportunity does not happen as often as it should.

### Setup
A new site should be set up in 2 locations
- Local – development
- You should create a new virtual host and begin constructing the site on the local domain. I have been using MAMP to do this, but there are a range of other tools.
Remote – testing
Log in to the Plesk panel for the server
Add a new subscription / account
Enter the domain as {project}.developmentdomain.co.uk
The Service Plan should be ‘default domain’
Contact details should be your contact details
All emails should go to 
Record all access information on the -LOCATION- -FOLDER-

### Coding Guidelines
I have produced a Contractor Guidelines document that you may like to review at -FOLDER-

This document outlines good practices for writing code that will be maintainable over the lifetime of a website. Please review this document regularly to keep it up to date and ensure that all contractors adhere to its principles.

Please also adhere to its principles yourself.

Add the following plugins to the site as soon as work commences; this will avoid potential conflicts that could occur if you add them later:
- Wordfence
- Broken Link Checker by Janis Elsts
- Simple 301 Redirects by Scott Nelle
- Jetpack

### Go Live
Only once the project has been approved by the client and approved by the account manager should it go live.

As soon as you have the appropriate login details for the target server, test that these work as expected before the launch date.

Before launch is attempted, it would be wise to consider doing it at a time that will be least disruptive to users, perhaps an early morning or evening.

Every effort should be made to reduce site outage. This can be done by redirecting the server to another location temporarily, or by use of a HTML holding page (and a 301 Redirect in the .htaccess file).

Please also ensure that you fill out a Launch Checklist prior to the date of launch and submit this to the Account Manager. This will enable deniability in the case of any obstructions that cause extended downtime.
Make sure you delete the .git folder, or avoid uploading it to begin with. This hidden folder contains history of your build and could compromise the security of the site.

The Launch Checklist is kept at -FOLDER-
Please don’t forget about adding Google Analytics tracking to the site.

---

## Editing an Existing Site
Occasionally a requirement will come in that adds functionality to an existing live site.
When doing this, the site should be duplicated on your local machine before commencing work. This will allow you to work without disrupting the site for users.

At every step of the way it is imperative that as little disruption to users of the site is caused. Site downtime costs clients money and harms our reputation.

This means being alert to testing your work thoroughly, both on your development environment AND once the changes are live.

You may judge that the work is sufficient to warrant a new test site on -DEVELOPMENT DOMAIN- (or because it requires client signoff before going live.

Before uploading any changes to the live site, first take a backup of the site and database so that you can roll back quickly if things go south.

Hotfixing is very dangerous.

Make no assumptions.

### Ongoing Monitor & Maintenance
There are 3 tiers of Monitor & Maintain packages. What services are included in which package you can find out by going to -FOLDER-

Most of the reporting is done automatically using Uptime Robot and Wordpress’ automated updater.
I have been researching how to use Jetpack to automate updates but since this can easily break a site, it is not currently recommended until further testing can be carried out.
Server Management
These are our current servers:
•
•

They are both -TYPE OF SERVER- servers running -OS- and are managed by -SYS ADMINS-

#### -SYS ADMINS-
-SYS ADMINS- can be contacted by -SYS ADMIN CONTACT DETAILS-
-SYS ADMINS- manage software updates, backup routines, plesk panel updates and all system administrator duties. If a server goes down they will respond very quickly.

#### DNS Server
e also has a DNS server. Many of our sites DNS are managed by this server. You can find the DNS settings by going to Subscriptions in the Plesk panel.

The information in this panel is not canonical. To verify that we definitely are the primary DNS for a domain, please use a service such as https://www.whois.net/ 

Our nameservers are:
-NAMESERVERS-

#### Backup Routines
Both servers have backup routines on the Plesk panel, as well as custom scripts.
-BACKUP ROUTINE DETAILS-

#### Disaster Recovery Process
A disaster recovery plan is in progress but has not been finalised.
The following plans need to be considered in isolation:
Offsite server malfunction (recoverable data)
Offsite server meltdown (no recoverable data)

Data recovery and reestablishment of DNS records is to be a priority. We are currently examining the possibility of a redundancy backup system. This article might prove useful: http://www.supportingadvancement.com/systems/data_backup/full_redundancy.htm  

---

## Useful Tools Directory

#### Research
- [Mozilla Developer Network](https://developer.mozilla.org/en-US/) 
- [PatternTap | ZURB Library](zurb.com/patterntap/)

#### Scoping
- [Online Diagram Software and Flow Chart Software - Gliffy](https://www.gliffy.com/)

#### Build Tools
- [Kraken Image Optimizer](https://kraken.io/)
- [The W3C Markup Validation Service](validator.w3.org/)
- [Google WMT Mobile-Friendly Test](https://www.google.com/webmasters/tools/mobile-friendly/)
- [YSlow](http://yslow.org/)
- [Pingdom Website speed test](tools.pingdom.com/fpt/)
- [Byte Check - Check Your Time To First Byte](www.bytecheck.com/)
- [Gzip compression testing tool](www.feedthebot.com/tools/gzip/)
- [Can I use...](caniuse.com/)
- [Statcounter Browser Stats](gs.statcounter.com/)
- [BrowserStack](www.browserstack.com/)
- [Browser-Update.org - Update your Browser](https://browser-update.org/)
- [WordPress Serialized PHP Search Replace Tool](https://interconnectit.com/products/search-and-replace-for-wordpress-databases/)

#### Server Tools
- [SSL Server Test (Powered by Qualys SSL Labs)](https://www.ssllabs.com/ssltest/)
- [SSL Check](https://sslcheck.globalsign.com/en_US)
- [Whois Lookup & IP](https://www.whois.net/)
- [Sucuri SiteCheck - Free Website Malware Scanner](sitecheck.sucuri.net/)
- [VirusTotal - Free Online Virus, Malware and URL Scanner](https://www.virustotal.com/en/)

#### DNS Tools
- [Global DNS Propagation Checker - What's My DNS?](https://www.whatsmydns.net/)
- [Network Tools: DNS,IP,Email](mxtoolbox.com/SuperTool.aspx)
- [SPF Query Tool](www.kitterman.com/spf/validate.html)

#### Monitoring Tools
- [Uptime Robot](https://uptimerobot.com/login)

#### Email Tools
- [eMail CSS Inliner](templates.mailchimp.com/resources/inline-css/)
