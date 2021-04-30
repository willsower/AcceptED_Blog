---
title: 'Preliminary Database Design'
date: '2021-04-29'
---

## Database Research
Before we design and impliment the database, we must determine what data is necessary. This is not yet finalized, but the design team has given us an idea of what we will need. I will be using the term entity to refer to a table in the relational database, and the term attribute to refer to the columns in that table.

All users have the following attributes:  
    Name (first + last)  
    Email  
    University Code  
    Password  
    Profile Photo  

From there, users diverge into two types: students and consultants. There are multiple ways to impliment this subclass structure in a relational database, but that is a problem for future me. See [this stackoverflow post](https://stackoverflow.com/questions/13749525/relational-database-design-multiple-user-types). For now, I need to list the data needed for each type, and consolidate any shared attributes into the main user entity.

**Walker**