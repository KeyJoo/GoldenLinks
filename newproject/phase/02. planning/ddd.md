# DDD

_CS618_

Domain-Driven Design: Tackling Complexity in the Heart  of 
Software   by Eric Evans

http://selab.netlab.uky.edu/homepage/CS618-DDD-Foundations.pdf


## Evans’ Layers (Isolating the Domain)

### User Interface Layer

• A.k.a. Presentation Layer
• Show Information
• Interpret commands

### Application Layer

• Thin layer, sirects UI commands to jobs in the Domain Layer
• Should not contain Business Rules or Knowledge
• No business “state”, may have progress “state”

### Domain Layer

• Business objects, their rules, and their state
• The majority of the book focuses here

###  Infrastructure Layer

• Generic technical capabilities to support the higher layers
• Message sending, persistence
• Supports the interactions between topmost patterns


## Download Book

[Download Book Eric Evans - DDD](http://sd.blackball.lv/library/Domain-Driven_Design_-_Tackling_Complexity_in_the_Heart_of_Software.pdf)