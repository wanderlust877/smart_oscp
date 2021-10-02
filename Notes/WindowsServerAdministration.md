## Windows Server Administration
## OS used: Windows Server 2012 r2

Windows Domain:

**What is a Windows Domain**

- Windows Domain is a Computer Network where user accounts, computer, resources and security are stored and defined on one or more servers called Domain Controllers
- Users and computers are authenticated on the Domain Controllers
- Permissions to resources are based on users and groups

**Setting up our Server with Active Directory Domain Service.**

- it is a role-based or featured-based installation.
- if we have multiple servers in our pools we could select them and install the service in those also if we want.
- Select Active Directory Domain Service and also select Group Policy Management Service in advanced that will help later.
- And the finally install it.
- Promote this server to a domain controller to take advantages active directory domain services
- Configure the Active Directory Domain Services:
	- you'll will find three options for Deployment operation:
		1. Add a domain controller to an existing domain 
		2. Add a new domain to an existing forest
		3. Add a new forest
	- Now above there is a new term **Forest** appears which basically means the collection of domains. And **Domains** is the computer network or the **Domain Controller** houses all the users, computer and resource information in a local directory, and **Forest** is simply a group of domains where there are separate groups of **Domain Controller** and all of that information is controlled on an individual per domain basis but all belong to the same **Forest**.
	- Now for the first time we don't have any **Forest**, so select the last Option which says ***Add a new forest***
	- Then Enter the Domain Name. (In a windows domain name context, it dosen't refer to an Internet Domain name but rather a record that all the computers and all of the users account we use to lookup resources within the Domain. There we need to use a domain that dosen't exist on the internet. A good practice is to use something ends in **.local** because this cannot be exist in public domain namespace.)
	- Now, we'll set the functional level of the new forest and root domain (The Functional level of a forest or a domain is simply a set of features that is allowed on a domain as a whole, this is mainly controlled by what versions of windows servers or active domain controllers within a domain).
	- There we've not much choice for now, but the default is good to go!
	- **Global Catalog**: is simply a record of all other resources that exist on the domain controller and advertised to all other users and computers based on their permissions. The Primary Domain controller is has to be the Global Catalog becuase it's the first that we are setting.
	- The Option **Read-only domain controller(RDDC)** is greyed-out and you can't enable it, because the first Primary Domain Controller is being setup and it's need to writable, later you can setup a Domain Controller that is **Read-only** for special purposes.
	- Now Set the Directory Services Restore Mode(DSRM) Password(it is used to recover the Directory services and Directory Information in case of a Disaster.)
	- Setup DSRM password and Click Next
	- When you first setup the Primary Domain Controller in a basic domain it could possible that this will prompt to you that **A deligation for the DNS server cannot be created because the autoritative parent zone cannot be found**, this is normal just click Next to continue.
	- Then we'll be asked to setup NetBIOS Domain Name (NetBIOS is basically the first part of root Domain name that we've set before) just leave as default and click Next.
	- Specifying the location of the AD DS database, log files, and SYSVOL (The Default for these Folders are just fine but for advance lessons you can modify the location of these folder) Click next with default and Continue.
	- Prerequisite Check: it contain the warning about security, read them all and scroll down to complete the Prerequisite Check and Click **Install** to install. 
***After the Completion of Installation we'll warned about to be signed out and the computer will be restarted.***

	
