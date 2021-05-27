---
title: "Cybersecurity Strategy for Early Stage Startups and Entrepreneurs"
author: Ashish Kumar
date: 2021-05-20
hero: ./images/hero-1.png
excerpt: Cybersecurity isn't the top priority agenda for early stage startups and entrepreneurs. Among others one reason is understanding of cybersecurity considerations when you're just starting up. This article aims to provide a practical and step by step plan to create cybersecurity stratgey for startups and entrepreneurs  .
---
## Why think about Cybersecurity right at the start of your entrepreneurial journey? 
Cybersecurity is not a problem of luxury anymore. Everyone has something valuable out in the digital world and the same applies even to an early-stage startup. As an entrepreneur or founder with competing priorities, you might not have given it too much thought. But it is far easier to embed the right cybersecurity habits right from the beginning than bolting it onto something which didn't have the right foundations. 

> One of my founder friends rang me up with surprise when his development environment was hacked within an hour of spinning up the server. What did I find? The security was overlooked and servers were left vulnerable by opening up to the World.

There have been instances where cloud subscriptions were misused for illegal activities such as bitcoin mining and founders were denied any reimbursement claims because they didn't take the right measures to secure their accounts.

<div class="Image__Small">
  <img src="./images/attacks-on-data.png" alt="Image showing common hacker attempts." />
  <figcaption>Hackers Are After Your Data</figcaption>
</div>

Even at the smallest scale, without any material impact, such incidents can be time-consuming and frustrating. In this post, I'll discuss some key considerations which can help you evolve and formulate your cybersecurity strategy - *__A plan of action.__*


## #1 Do you know your data and assets? 
May seems like an obvious answer, but it is always better to think this through. A simple spreadsheet would do where you can record details such as:
* Your intellectual properties — Business plans, Marketing strategy, Critical emails, Technology code etc.
* Customer Data including PII
* Keys to your kingdom — business account details, bank details, passwords etc. 

__*Why is this important?*__ You can't protect it unless you are aware of it. Data is the gold after which the bad guys are. Once I know my assets, I can assess what protection needs to be built around them. That brings us to our next point.

## #2 Adequate protection for your data and assets
For early-stage startups, founders and entrepreneurs the spread of your digital footprint might not be that widespread yet. Once there's clarity on your digital data, a pragmatic assessment of the effort required to protect that data can be done.

You may have created something like below in the first step:

| Data/Asset Type                                                                                                                                                                                                                                                                              | Resides At                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Emails                                                                                                                                                                                                                                                                                       | - Email provider online <br />- Downloaded in laptop <br />- Backed up in external hard-drive                                                                                                                                                        |
| Plans, documents, contracts                                                                                                                                                                                                                                                                  | - Email provider online <br />- Downloaded in laptop <br />- Backed up in external hard-drive                                                                                                                                                        |
| Development Code                                                                                                                                                                                                                                                                             | - Laptop as the development environment <br />- Online code repository such as Github                                                                                                                                                              |
| Subscriptions such as: <br />- Bank details <br />- Online platforms and services such as Stripe account, Shopify account etc. <br />- Cloud or virtual technology platforms such as AWS, Netlify, DigitalOcean etc. <br />- Filesharing such as dropbox <br />- Notetaking such as Evernote | Mostly the details would reside on your personal laptop                                                                                                                                                                                            |
| Passwords                                                                                                                                                                                                                                                                                    | Mostly the details would reside on your personal laptop                                                                                                                                                                                            |
| Customer Data                                                                                                                                                                                                                                                                                | - With online service provider such as Shopify, Zendesk etc. <br />- In the customer database of your application <br />- On your laptop, in a spreadsheet for some analysis <br />- One of file-shares for sharing with partners, developers etc. |


If you understand the exercise above, your data spread has three key themes:
* Password is the key for all the data residing at subscription services
* Laptop is the most vulnerable place where most of the data would be available without additional protection
* A vulnerable application and insufficient access controls to your servers and database could lead to data theft.

## #3 Secure Start 
"Secure start" is all about staying on a path that enables you to achieve whatever your cybersecurity maturity goal is. Your goals may keep changing as the business evolves. Regulatory compliance, GDPR requirements, PCI/DSS certification etc. are examples of reasons why your objectives would keep getting broader.

Continuing with the conversation in the previous section, there are small actions that may have a major impact:

### Strong Authentication and Password Security
* Almost all online services allow multi-factor authentication. There's no excuse to not use it. And if you're using a service in this day and age which doesn't have it then re-evaluate that relationship. Move to services that have given security some priority.
* Use password managers to store password. Google the topic if you're unfamiliar with the idea.

### Use Platforms (SaaS/Paas) to Build Application and Service
* Use Website Builders, Software-As-A-Service (SaaS) or low-code PaaS where possible to run your business. Maintaining servers and other infrastructures such as database requires specialized skill which may not be your core suite. For example, prefer Shopify or Squarespace for your e-commerce instead of using custom-configured WordPress deployed on a server provided by a hosting service. As another example, this blog website is deployed on Netlify using static-website-generator Gatsby. There is essentially no server-side processing and all I need is read-only code distributed via CDN.
* Read provider documentation on how to secure services. Always review your privacy and security settings to tune them for the best possible use.

### Secure Application Development
* Not everyone's requirement fits into limitations offered by platform services. You may end up building your custom application stack.
* Awareness and the right tools are your friends here. It wouldn't hurt to invest in understanding the basics of application security and secure code development. Google search should be the go-to resource.
* Familiarize yourself with OWASP ([www.owasp.org](https://owasp.org)). You may find tools that can aid your secure development process [here](https://owasp.org/www-community/Free_for_Open_Source_Application_Security_Tools).

### Secure Deployment
* Application needs to be deployed before it can be used by your audience. Deploying an application stack is a complex process. You may need to think about things like:
```
- CDN
- DNS
- Encryption (network, storage)
- SSL Certificates
- Load Balancer
- Web Server/Container/Web Functions ⬅ THAT'S WHERE YOUR APPLICATION WOULD LIVE
- API Gateway
- Database
```
> The complexity could be more or less depending on your exact requirements, but the key point to understand that each of these components or aspects of your "solution" would require some secure configurations of its own.

* Some things which could help
  * Established cloud service providers give many of these as "managed services", which means you'd have less to worry about. Leverage that where possible.
  * Restrict access to services wherever possible. Use the principle of least privilege. For instance, you don't need to expose a database to the whole world. Only middleware needs to have access to DB.
  * Use VPN or some other form of a session management system that allows a secure connection between your laptop and servers/infrastructure. If you're setting up a VPN of your own, always be patched up, restrict IPs from where connection can originate and always use additional authentication methods.
  * Take help from an expert, this can be daunting.

## #4 Secure Endpoint (Laptop/Workstations/Servers)
* I suppose I don't need to stress the importance of protecting your laptop and data residing within. Think about threats such as system crash/fault, virus or malware (ransomware), theft or loss etc.
* Operating system should always be patched.
* Invest in modern Anti-virus/Anti-malware software. Preferably, one which gives benefits such as URL filtering and scanning.
* Back up your code, important files, keys etc. regularly. Use an automated mechanism to do a daily backup to a cloud service or the local disk. Storage is cheap so have rolling and redundant backups i.e. you can go back to different versions of backup.
* Password-protect your laptop and encrypt your drive so that in case you lose it, the data shouldn't be recoverable without the password.
* If you've servers, then they also need to be protected appropriately —  virus, malware, host-intrusion, host-firewall, application whitelisting, logging to be considered at minimum.

## #5 Backup, Monitoring, Logging 
* Backup regularly, that's the only hope of recovering in case of a mishap.
* As suggested earlier, use configurations only platforms wherever possible. Keep a screenshot or record of your settings.
* Test whether restore actually works.
* Keep a track of logs from various services, this is applicable when you've deployed your custom stack. If you can't build scripts to automate the detection of anomalies then manually inspect at a regular interval or whenever there's a suspicious service degradation.
* Monitoring your services is always a good idea. Helps you know your failures before your customers notice.

> If you've built your application and deployed the stack, invest some capacity to set up basic monitoring and log automation. Would pay off in terms of resiliency.

## #6 Think How Would You Respond To a Cybersecurity Incident? 
* So you've done everything right and shit happens! What do we do now? Think it through:
  * Your laptop is encrypted by ransomware, encounters a system-level crash, stolen or lost.
    * Key files should be backed up.
    * Passwords recovered via Password Manager
    * Code stored in online repo such as GitHub
    * Contracts copy in email and backup hard-drive
  * Your website is defaced, taken down, hacked and serving inappropriate content
    * Have mental or documented playbooks ready to refresh the deployment - rebuild, redeploy
  * Key online services and accounts were taken over
    * Use password reset and log everyone else out.
    * If nothing else, reach out to your service provider immediately.
  * Hit by a web-attack
    * Your cloud service provider, webmaster should be able to help.
    * If you're alone responsible for what happens to your service then there's not much you can do apart from talking to provider/ISP to deflect the attack by blocking source etc. Else just shut down and wait.

So, there it is. I realized that the post became longer than I originally thought, but I hope it provides value to someone.

> Remember, hackers, adversaries and bad guys are opportunists. They don't have anything against "you". If you're making their job 10% harder, they'll move on to the next target.


Image Attributions:
* *Hero Image:* [Technology vector created by macrovector - www.freepik.com](https://www.freepik.com/vectors/technology)
* *Hackers Are After Your Data*: [Technology vector created by freepik - www.freepik.com](https://www.freepik.com/vectors/technology)
