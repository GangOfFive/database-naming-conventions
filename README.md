**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [Database naming conventions for Gang of Five](#database-naming-conventions-for-gang-of-five)
	- [Tables](#tables)
	- [Attributes](#attributes)

# Database naming conventions for *Gang of Five*

## Tables
 - All tables should have an id attribute, which is their primary key.
 - Table names should be plural, in lowercase, separating words with an underscore:
   - `users`
   - `permissions`
   - `roles`
   - `private_messages`
  - Tables used for relationships should named as follows: `table1_table2`.

## Attributes
 - Same naming conventions as table names.
 - If an attribute is a foreign key, it should be named singular as follows: `table_id`.
   For example, if the `private_messages` table has a foreign key for user,
   the foreign key should be named `user_id`.
