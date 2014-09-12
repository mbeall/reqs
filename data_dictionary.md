# Data Dictionary
_Table and column information for the database._

## users

| Column  | Datatype    | PK | RQ | UQ | FK | Description |
|---      |---          |--- |--- |--- |--- |---          |
| user_id | INT         | X  | X  |    |    | Unique identifier for each user; automatically generated. |
| user_ip | VARCHAR(15) |    | X  |    |    | The IP address identifying the user. |

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

| Column          | Datatype     | PK | RQ | UQ | FK | Description |
|---              |---           |--- |--- |--- |--- |---          |
| team_id         | INT          | X  | X  |    |    | Unique identifier for each team; automatically generated. |
| team_owner_id   | INT          |    | X  |    | X  | The owner or administrator of the team: references `users.user_id`. |
| team_name       | VARCHAR(32)  |    | X  |    |    | A team's name. |
| team_desc       | VARCHAR(255) |    |    |    |    | A description of the team. |

## team_members

| Column         | Datatype     | PK | RQ | UQ | FK | Description |
|---             |---           |--- |--- |--- |--- |---          |
| team_member_id | INT          | X  | X  |    |    | Randomly generated number that identifies team membership. |
| team_id        | INT          |    | X  |    | X  | The team that a user is a member of: references `teams.team_id`.  |
| user_id        | INT          |    | X  |    | X  | The user that is a member of a team: references `users.user_id`. |
| user_role      | VARCHAR(32)  |    | X  |    |    | A user's role on the team. (i.e. team lead, team member, etc.) |

