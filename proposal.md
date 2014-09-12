# Project Proposal
## Description
Our website will be a support ticketing system that can be used for a variety of software, projects and organizations. While the project may expand in the future, there will be two basic types of users of the website: administrators and customers. Customers will be able to submit issues and feature requests for software and other projects without needing to create an account. Instead, they will verify which software/project/organization they are submitting a ticket for via a unique URL. Administrators will be able to login and moderate tickets, assigning tags, priorities, and support staff to them.

## Functionality
- Customer: Submit a ticket for a problem encountered with the software, project, or organization.
- Customer: Submit a feature request for the software, project, or organization.
- Customer: Submit a screenshot to help administrators replicate an issue.
- Customer: Search for open tickets.
- Administrator: Assign tickets to other administrators on the same software, project, or organization team.
- Administrator: Assign tickets a priority (High, Medium, and Low).
- Administrator: Assign tickets a custom tag (i.e. css, js, docs, examples, etc.).
- Administrator: Assign and track tickets by status (Open, In Progress, Resolved, etc.).

## Business Rules
- Administrators can only access projects that they create or have been invited to administer.
- Customers will be encouraged to register, or at least provide their name and email address, but it is not required.
- Unregistered users' activity will be logged under their IP Address.
- Unregistered users will only be able to submit x amount of tickets in a 24-hour period.

## Assumptions
- Submitting a ticket needs to be as simple as possible for the customer, requiring the smallest amount of information possible.
- Not all customers wish to be followed up with.
- Ticket moderation, management, and customer support should be easy to manage for administrators.
- A system that is not cumbersome for customers AND not cumbersome for administrators IS POSSIBLE.
- The customer knows how to navigate a website.
- The customer will be affiliated with the company.
- The customer has a goal in mind for what they are looking for.
- The customer is comfortable entering basic information on the website.
- The customer is comfortable with the website tracking their IP address and other identifying information.

## Web Pages

#### Home
On the home page will be a brief introduction to what the website/application does and will have an area to login for administrators. There will also be a link to the About and Contact pages, and the option to search for a user, project, or organization.

#### Contact
The contact page will be a simple contact form that allows administrators and customers to contact us.

#### About
On the About page, the website/application will be described in detail, including features and possibly some “How To” links or content.

#### Organization/Team Profile (administrator)
The profile page shows all the projects and administrators for a particular organization or team. It may also give a summary of recent tickets for a project or administrator.

#### Project Page (administrator)
The project page will show a list of all the tickets, with the ability to sort the tickets based on date, priority, tag, status, or assigned administrator. From this page, the administrator can navigate to the individual ticket view, or assign priority, tag, status, or administrator directly from this view. Only the first few words and/or title of the ticket will be displayed on this page; to see the rest of the text for a ticket, it is necessary to navigate to the individual ticket view.

#### Project Page/Ticket Form (customer)
For any user not logged in, the project page will display a search field and a basic form. The search field is for the customer to verify that their issue or request has not been submitted already, and if it has been resolved. The basic form will allow them to submit a new ticket.

#### Ticket View
An individual ticket is displayed with status, tags, priority and assigned administrator information.

The flow of the website will follow the order from above.

## Validation
- Customers will be required to answer a math or CAPTCHA problem to verify that they are human.
- Customers who have blocked accounts or IP Address(es) will not be able to submit a ticket.
- Each ticket will have requirements that need to be filled out before it can be submitted. 
- Spell check will be built into the website.
- The website will check each field has the correct data type entered.

## Database Schema
- [Database Diagram] (https://github.com/c410echo/reqs/blob/master/c410ed.png)
- [Data Dictionary] (https://github.com/c410echo/reqs/blob/master/data_dictionary.md)

## Model Sites
- [GitHub.com] (https://github.com)
- [Waffle.io] (https://waffle.io)
- [Trac] (http://trac.edgewall.org)
- [Travis CI] (https://travis-ci.org)

## Database Details
_This information will not available on GitHub_
