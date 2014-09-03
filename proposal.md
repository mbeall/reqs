# Project Proposal
## Description
Our website will be a support ticketing system that can be used for a variety of software, projects and organizations. While the project may expand in the future, there will be two basic types of users of the website: administrators and customers. Customers will be able to submit issues and feature requests for software and other projects without needing to create an account. Instead, they will verify which software/project/organization they are submitting a ticket for via a unique URL or some other method. Administrators will be able to login and moderate tickets, assigning tags, priorities, and support staff to them.

## Functionality
- Customer: Submit a ticket for a problem encountered with the software, project, or organization.
- Customer: Submit a feature request for the software, project, or organization.
- Customer: Submit a screenshot to help administrators replicate an issue.
- Administrator: Assign tickets to other administrators on the same software, project, or organization team.
- Administrator: Assign tickets a priority (High, Medium, Low).
- Administrator: Assign tickets a custom tag (i.e. css, js, docs, examples, etc.).
- Administrator: Assign and track tickets by status (Open, In Progress, Resolved, etc.).

## Business Rules
_A preliminary list of the rules that will govern your application._

## Assumptions
_Assumptions (if any) that you have made about who will use your application and how they will use it._

## Web Pages
_A preliminary list of web pages. For each page, a brief description of its purpose and a written or graphic representation of its layout and contents. The proposed flow among the pages should also be included._
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

Note: This is NOT an exhaustive list.

## Validation
_A preliminary list of the validation checks that will be performed on input data._

## Database Schema
_A preliminary list of normalized tables that will be required to support your application. For each table, its fields (name, data type and description) should be provided. Primary and foreign keys should also be clearly identified._

## Model Sites
- [GitHub.com] (https://github.com)
- [Waffle.io] (https://waffle.io)
- [Trac] (http://trac.edgewall.org)
- [Travis CI] (https://travis-ci.org)

## Database Details
_A name for your database, and a username and password (simple and weak)._
