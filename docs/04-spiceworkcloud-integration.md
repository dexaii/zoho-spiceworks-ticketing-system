# Spiceworks Cloud Helpdesk Integration with Zoho Mail Server
Note: this document outlines the integration ( in my case simulation **due to Spiceworks Cloud Free software Limitations** ) between Spiceworks Cloud Helpdesk, SaaS that acts as a ticketing system and Zoho Mail server. Details how Spiceworks Cloud was configured for the help desk functionality, including organization settings, ticket categories, roles, ticket routing, canned responses, and ticket management rules.

## Spiceworks Cloud Help Desk Configuration
Steps taken to setup a functional support ticket system for Dexaii Tech

**1. Creating an Organization:** Organization in Spiceworks works as a workgroup - it is a container for all of your users, tickets, and rules. Also, Spiceworks handles for you custom Help Desk URL, Portal URL, and Email. that has a structure `https://<your domain>.on.spiceworks.com/portal`

* Provided Spiceworks email `help@dexaii.on.spiceworks.com`is fully functional, which means it can be used to recieve/send messages

![Organization-setup](./screenshots/spiceworks/Organization-setup.png)

**2. Creating Custom Ticket Categories:** To organize and classify the incoming requests (tickets) I have created ticketing categories.

` Settings > Organizations > [Your organization] > Ticket categories`
 * After creating a ticket category you can select the category upon ticket creating process. A few examples of created categories:
 * **Hardware Issues:** for problems related to physical devices, equipment, or peripherals devices
 * **Software Issues:** for any software or application-related issues
 * **Account & Access:** for manipulations with user accounts and permissions

![Ticketing-categories](./screenshots/spiceworks/Ticketing-categories.png)

## Roles and Ticket Assignment
Spiceworks Cloud supports multiple user roles for help desk staff, each with different permissions:
* Tech - Limited ticket and settings access
* Manager - Full ticket access. Limited settings access
* Admin - Full access
Roles and Permessions can be configured : `Settings > Employee Administration > Add Employee ` | Spiceworks Cloud has a **limit of 5 free accounts**

![Role-and-Permissions-assignment](./screenshots/spiceworks/Role-assignment.png)

## Canned Responses
