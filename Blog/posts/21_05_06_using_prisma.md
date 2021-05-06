---
title: 'Using Prisma'
date: '2021-05-06'
---

## What is Prisma?
Prisma is an Object-Relational Mapping tool. It allows us to modify a database using object-oriented style scripts rather than SQL, and prevents SQL injection. It also has a GUI where we can view and modify values in the database.

## How does it work?
See [this tutorial](https://vercel.com/guides/nextjs-prisma-postgres) for detailed setup information.  
To create the database schema, we use the schema.prisma file. In this file we define the following:
* datasource: this has provider, which we will set to "posgresql", and url, which will be the url of our database
* generator: has provider, set to "prisma-client-js" because we are using next.js
* models: these are the tables in the database. Each line within a model has the name of the attribute, the type (with a question mark if it can be null), and other parameters, such as "@relation", which defines a relation to another table.

When that is set up, we must set up a prisma client. The client is a query builder that prevents SQL injection and organizes our queries.  
[Here is the prisma API reference](https://www.prisma.io/docs/concepts/components/prisma-client). I will use this often when building queries.
As we build the project, I will become more familiar with the structure and syntax of Prisma queries. These Prisma queries are wrapped in javascript functions, which can then be called by the frontend team to get the data they want to display.
**-Walker**