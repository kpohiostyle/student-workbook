# Day 3 DOTNET WEBAPI Review
## Daily Journal
Read Dotnet WebAPI's > SQL Injection, and answer the following questions
## What is SQL injection?
    Injection is a attack on your application database by inserting arbitrary SQL code into a db query. It is very easy to either attack or defend.

## What are 3 methods SQL injection can be done by?
    One method of SQL injection attacks is through user input fields. Another method of injection is by "poisoning cookies" This means an attack can modify a cookis to inject SQL into the back-end database. Forged headers that contain arbitrary SQL can inject that code into the database if the app fails to sanitize the HTTP header.

## How can we detect and sanitize SQL injection attacks?
    First we can use detection blockers such as a web application firewall or an intrusion detection system. Then we can whitelist input validation, limit account privileges and using stored procedures can help sanitize SQL injection.
## Afternoon Challenge
    https://github.com/ThurberDaniel/AllSpice
