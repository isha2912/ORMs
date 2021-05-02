As a relative newcomer to the programming world, terms like Object-Relational-Mapper can sound really intimidating. The nice part about ORMs, is that they actually make it easier to write code once you get the hang of them (usually).

As a relative newcomer to the programming world, terms like Object-Relational-Mapper can sound really intimidating. The nice part about ORMs, is that they actually make it easier to write code once you get the hang of them (usually).

Recently, the NestJS framework has been gaining extreme popularity due to its incredible features. Some of them are:

It leverages TypeScript - strongly typed language which is a superset of JavaScript
Easy to use, learn and master
Powerful Command Line Interface (CLI) to boost productivity and ease of development
Detailed and well-maintained documentation
Active codebase development and maintenance
It is open-source (MIT license)
Support for dozens of nest-specific modules that help you easily integrate with common technologies and concepts like TypeORM, Mongoose, GraphQL, Logging, Validation, Caching, WebSockets and much more
Easy unit-testing applications
Created for Monoliths and Micro-services (an entire section in the documentation regarding Microservice types of NestJS applications as well as techniques and recipes

Well, an Object-Relational-Mapping tool basically takes away the pain (perceived) of writing SQL. As object-oriented programmers, we tend to think in terms of objects.

An ORM tool keeps your object model separate from your persistence model, i.e., your java code need not know about your database tables. You write your data modification code in a programming language of your choice and the ORM tool will map that to the database for you.
In most cases, you don’t have to write much SQL and you really don’t end up writing SQL that caters to a specific database vendor (in the highly unlikely case that you decide to switch databases after writing an application).
ORMs also take away the repetitive, mind-numbing job of writing code that maps object properties to columns and vice-versa.

Wait. If the only reason you really like ORMs is that they help you avoid SQL, you will eventually be stuck up the proverbial creek without a paddle.

While they do reduce development time, there is a bit of a learning curve.
For most non-trivial projects, where you have to do more than simple CRUD, ORMs don’t perform quite as well as simple SQL.
Badly written application code (the most common kind!) also means that changes to the database will not be transparent to your object model and your application will have a severe case of the shits. -Caching, concurrency support etc. are not really features of an ORM and can be dropped into any application.
In short, if you have a simple project with a none-too-complex object model, use simple JDBC. If you have a complex domain model with ‘interesting’ relationships between the objects, use an ORM.

At some point, however, you will need to tune your application to cater to higher loads and replace some of that auto-generated SQL with something more efficient – which means that if you’re writing an application that uses a relational database you’d better !$@!%@#$% know SQL.

ORMs help to reduce the Object-Relational impedance mismatch. They allow you to store and retrieve full live objects from a relational database without doing a lot of parsing/serialization yourself.

What does it give me as a developer?

For starters it helps you stay DRY. Either you schema or you model classes are authoritative and the other is automatically generated which reduces the number of bugs and amount of boiler plate code.

It helps with marshaling. ORMs generally handle marshaling the values of individual columns into the appropriate types so that you don't have to parse/serialize them yourself. Furthermore, it allows you to retrieve fully formed object from the DB rather than simply row objects that you have to wrap your self.
