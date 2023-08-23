#cloud #azure #az-104 #professional 

## Identity
- ### Azure AD 
	- identity provider for the cloud. 
	- Supports multiple protocols 
		- OpenID Connect
		- SAML
		- WS-FED
		- OAuth2
	- Communicates over HTTPS
	- Uses MS Graph and REST API's
	- Start with a "Tenant" and comes with a domain
	- Custom branding available
	- Guest Accounts
		- Other AAD
		- Microsoft Accounts
		- Gmail Accounts
	- Can use "Bulk Create"; PowerShell
		- Can also use Dynamic Groups and create rules based on attributes and tags
	- Preferred way of doing things is to create a group, assign permissions to the group, then add users to the group
	- #### Subscriptions
		- Does not live a subscription. 
		- Subscriptions will TRUST a specific AAD ("Directory")
		- Permissions for resources within a subscription can use AAD objects to assign permissions to groups within the subscription.
	- #### Roles
		- Lots of built in roles that can either be general or app-specific
		- Applied to the entire tenant
			- Administrative Unit
				- Creates sub-units off of the flat architecture to assign roles to a smaller subset of the tenant.
					- Groups added to an administrative unit can be managed, but the members of that group cannot be managed. 
					- If you want to manage the users of the group then those users need to be added to the AU separately
	- #### InTune
		- Can leverage permissions and controls for remote devices to ensure that appropriate gates are mets before giving access to certain areas of information
- ### On-Prem AD
	- Uses different protocols that don't work well over the internet
		- Kerberos
		- NTLM 
		- LDAP
	- Can use Azure AD Connect (Cloud-Sync) to replicate on prem-AD to Azure AD
		- This is a one way flow from On-prem to the cloud, not from the cloud to on-prem
		- Shows up as "Directory Synced"

## Subscriptions
- ### Management Groups
	- Level between Subscription and Resource Groups
	- Has the same management capability as Subscriptions
- ### Resource Groups
	- Organizational structure that houses resources
	- Organize items in a RG that has a common lifecycle
	- Each RG can have its own permissions and management structure
	- Can assign budgets at the RG level
- ### Tags
	- Can be used to add meta data to items
	- Tags are not inherited down, they need to be applied to all items individually.
		- This can be remedied through the use of policies to pull tags from higher up int he architecture
- ### RBAC
	- Scope is the assignment of a ROLE to a IDENTITY
		- Can be set at various levels(Sub, RG, MG, etc.)
		- Owner: add, edit, delete, manage
		- Contributor: add, edit, delete
		- Reader: read-only
		- #### Control vs Data Plane
			- Interface with the Azure Portal and normal management functions are performed by the user as part of the Control Plane
			- These actions call API's to the Data Plane which then implements those changes
			- Can add custom roles
			- Activity log can track what is happening at the DATA PLANE level
		- Want to use broad permissions at the highest level and get more narrow as you get lower in the architecture

## Cost Management
- ### Budget
	- Set limits 
	- Can send emails, resize, or other actions to limit over spending
	- Can be set at various levels (Sub, RG, MG, etc.)

## Policy
- Enables self-service guard rails to establish what restrictions in order to ensure proper governance is in place.
- Can be enabled at various levels (sub, RG, MG, etc.)
- Generally starts with an initiative
	- Creates Policies
		- Can narrow down application through Parameters (though Azure Policy)

## Regions
- "Latency Envelope"
- Made up of multiple data centers, minimum of 3
- There are multiple clouds; Commercial, Gov, China, German 
- Regions have "Region Pairs" that they can replicate to.
- ### Availability Zone
	- Separate data centers to ensure system availability is maintained.
	- Zone-redundant = resilient; automatically deploys to multiple AZ's
	- Zonal = only in a specific AZ; requires deployment into different AZ's manually

## Networking
- Primarily pay for egress, not ingress
	- If you connect on-prem networks to Azure, you pay for ingress
- ### Virtual Network
	- Lives within a certain Sub and Region. 
		- Cannot span subs or regions
	- IPv4 CIDR or IPv6 CIDR
		- IPv6 requires at least (1) IPv6 subnet
	- Common to use RFC 1918 (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16)
		- Can bring your own, but still will be a private IP range
		- Dont pick the same IP range as other vNETs
		- Dont pick the same IP range as being used on-prem
	- Each subnet looses 5 IPs (network, broadcast, gateway, dns1, dns2)
	- Resources can by default access the internet but cannot be access from the internet
		- Would need to assign a Public IP through the application of a load balancer with Firewall
		- Public IPs are bound by region. Cannot be moved from region to region
			- Standard = static, zone redundant
				- Want to use a "standards" LB with it
			- Basic = static or dynamic
	- DHCP
		- Resources will ALWAYS use DHCP, but you can set IP reservations for specific resources 
	- Peering
		- Point to point connectivity between multiple vnets
		- MUST be different IP ranges

