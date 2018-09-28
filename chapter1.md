# 

# Data Models and Query Languages

The state of our data models shows how we think about a problem. It also has impact on our ability to handle a problem. For example, there is a big difference when we relation or document oriented database.

When we have a model persisted in relation database, it is difficult to represent it and work with in an object oriented language. Sometimes, the model can become too granular in relational database and there are many tables that have relation to each other. That can be a good think, when it comes to consistency, performance or localization support. But it becomes more complext to build a query that provides complete data for user. On the other hand, document can store all the data in single document, but it becomes technically challanging to join documents on database level. It can seems reasonable to use document oriented database at the beggining, but as the application evolves, inability to join documents can become technical bottleneck.

When many-to-many relationships are very common in our data model, we might want to use graph database.



