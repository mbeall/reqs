# Data Dictionary
_Table and column information for the database._

## users

| Column  | Datatype    | PK | RQ | UQ | FK | Description |
|---      |---          |--- |--- |--- |--- |---          |
| user_id | INT         | X  | X  |    |    | Unique identifier for each user; automatically generated. |
| user_ip | VARCHAR(46) |    | X  |    |    | The IP address identifying the user. |

## reg_users

| Column          | Datatype    | PK | RQ | UQ | FK | Description |
|---              |---          |--- |--- |--- |--- |---          |
| user_id         | INT         | X  | X  |    | X  | Unique identifier for each user: identified by `users.user_id`. |
| user_first      | VARCHAR(32) |    |    |    |    | A user's first name. |
| user_last       | VARCHAR(32) |    |    |    |    | A user's last name. |
| user_email      | VARCHAR(64) |    | X  | X  |    | A user's email address. |
| user_login_name | VARCHAR(32) |    | X  | X  |    | A user's username used to login. |
| user_pass       | VARCHAR(32) |    | X  |    |    | A user's password used to login. |

## teams

| Column    | Datatype     | PK | RQ | UQ | FK | Description |
|---        |---           |--- |--- |--- |--- |---          |
| team_id   | INT          | X  | X  |    |    | Unique identifier for each team; automatically generated. |
| user_id   | INT          |    | X  |    | X  | The owner or administrator of the team: references `reg_users.user_id`. |
| team_name | VARCHAR(32)  |    | X  | X  |    | A team's name. |
| team_desc | VARCHAR(255) |    |    |    |    | A description of the team. |

## team_members

| Column         | Datatype     | PK | RQ | UQ | FK | Description |
|---             |---           |--- |--- |--- |--- |---          |
| team_member_id | INT          | X  | X  |    |    | Unique identifier for team membership; automatically generated. |
| team_id        | INT          |    | X  |    | X  | The team that a user is a member of: references `teams.team_id`.  |
| user_id        | INT          |    | X  |    | X  | The user that is a member of a team: references `reg_users.user_id`. |
| user_role      | VARCHAR(32)  |    | X  |    |    | A user's role on the team (i.e. team lead, etc.); default is `'member'`. |

## projects

| Column       | Datatype     | PK | RQ | UQ | FK | Description |
|---           |---           |--- |--- |--- |--- |---          |
| project_id   | INT          | X  | X  |    |    | Unique identifier for a project; automatically generated. |
| team_id      | INT          |    | X  |    | X  | The team that owns the project: references `teams.team_id`. |
| project_name | VARCHAR(32)  |    | X  | X  |    | A project's name or title.  |
| project_desc | VARCHAR(255) |    |    |    |    | A description of the project. |

## project_users

| Column          | Datatype     | PK | RQ | UQ | FK | Description |
|---              |---           |--- |--- |--- |--- |---          |
| project_user_id | INT          | X  | X  |    |    | Unique identifier for project participation; automatically generated. |
| project_id      | INT          |    | X  |    | X  | The project that a user is participating in: references `projects.project_id`.  |
| user_id         | INT          |    | X  |    | X  | The user that is participating in the project: references `reg_users.user_id`. |
| user_role       | VARCHAR(32)  |    | X  |    |    | A user's role on the project (i.e. project lead, etc.); default is `'moderator'`. |

## tickets

| Column          | Datatype     | PK | RQ | UQ | FK | Description |
|---              |---           |--- |--- |--- |--- |---          |
| ticket_id       | INT          | X  | X  |    |    | Unique identifier for a ticket; automatically generated. |
| project_id      | INT          |    | X  |    | X  | The project that the ticket belongs to: references `projects.project_id`. |
| user_id         | INT          |    | X  |    | X  | The user that opens the ticket: references `users.user_id`. |
| admin_id        | INT          |    |    |    | X  | The user that is responsible for resolving the ticket: references `reg_users.user_id`.  |
| ticket_name     | VARCHAR(32)  |    | X  | X  |    | A ticket's name or title. |
| ticket_desc     | VARCHAR(255) |    |    |    |    | A description of the ticket. |
| ticket_priority | VARCHAR(8)   |    |    |    |    | The priority for the ticket (i.e. High, Medium, Low) |
| ticket_status   | VARCHAR(8)   |    |    |    |    | The status of a ticket (i.e. Open, Closed, In Progress) |

## tags

| Column    | Datatype     | PK | RQ | UQ | FK | Description |
|---        |---           |--- |--- |--- |--- |---          |
| tag_id    | INT          | X  | X  |    |    | Unique identifier for a ticket; automatically generated. |
| tag_name  | VARCHAR(32)  |    | X  |    |    | A tag name. |
| tag_color | VARCHAR(6)   |    |    |    |    | The text color used for the tag: default is `ffffff`. |
| tag_bg    | VARCHAR(6)   |    |    |    |    | The background color used for the tag: default is `777777`. |

## ticket_tags

| Column        | Datatype     | PK | RQ | UQ | FK | Description |
|---            |---           |--- |--- |--- |--- |---          |
| ticket_tag_id | INT          | X  | X  |    |    | Unique identifier for tag/ticket relationships; automatically generated. |
| ticket_id     | INT          |    | X  |    | X  | The ticket being tagged: references `tickets.ticket_id`.  |
| tag_id        | INT          |    | X  |    | X  | The tag applied to a ticket: references `tags.tag_id`. |
