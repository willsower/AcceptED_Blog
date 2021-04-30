---
title: 'Preliminary Database Design'
date: '2021-04-29'
---

## Database Research
Before we design and impliment the database, we must determine what data is necessary. This is not yet finalized, but the design team has given us an idea of what we will need. I will be using the term entity to refer to a table in the relational database, and the term attribute to refer to the columns in that table. Values will refer to the actual data in the attributes.

All users have the following attributes:
* ID (primary key)
* First Name
* Last Name
* Email
* University Code
* Password
* Profile Photo
* Join Date (date their account was created)
* Type (Consultant or Student) - might not be needed, depending on the approach to relational "subclasses"

From there, users diverge into two types: students and consultants. There are multiple ways to impliment this subclass structure in a relational database \(see [this stackoverflow post](https://stackoverflow.com/questions/13749525/relational-database-design-multiple-user-types)\), but that is a problem for future me. For now, I need to list the attributes needed for each user type, and consolidate any shared attributes into the main user entity.

PostgreSQL supports arrays, so we can store multiple values in a single attribute.

Consultant attributes:
* University ID
* ID Photo (not to be confused with user's primary key ID)
* Tasks - array of Task IDs
* Students - array of User IDs
* Materials - array of Material IDs (this may need to be consolidated with Tasks)

Student attributes:
* High School
* Email opt-in
* Universities - array of StudentUniversityOption IDs
* Preferred Language

StudentUniversityOption attributes:
* IDs
* University ID
* Likelihood (Likely, Possible, Reach)
* Status (Waiting, Accepted, Rejected)

University attributes:
* ID
* Name
* Placeholder (if no other attributes are needed, we don't need University to be its own attribute)

Task attributes:
* ID
* Name
* Assigned Date
* Due Date
* Status (Not Started, In Progress, Complete)
* Files - Array of Material IDs (Unsure about this)

Material attributes: (These may change depending on the degree of Google Drive integration)
* ID
* Name
* Description
* Link
* Pinned (y, n)
* Folder (in main folder if Null)
* Type (Resources, Cirriculum)


I will complete these attribute lists and tackle organizing the cirriculum structure in another blog.

I also need to communicate with the design team about how Modules should work. Is a Module a set of Tasks, or is there more to it?

**-Walker**