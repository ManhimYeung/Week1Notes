# Agile notes

### What is it?

Ultimately, Agile is a mindset informed by the Agile Manifesto¡¦s values and principles. 
Those values and principles provide guidance on how to create and respond to change and how to deal with uncertainty.

##### Agile Topics
* [SDLC Models](#SDLC-Models)
* [Agile Pros and Cons](#Agile-Pros-and-Cons)
* [Agile Manifesto](#Agile-Manifesto)
* [Scrum Framework](#Scrum-Framework)

### SDLC Models
* The Waterfall Model
* The V-Model Wait for Joe to explain
* Incremental

### The Waterfall Model

![Water Fall](https://media.licdn.com/dms/image/C4D12AQHbOzu3Pk9dOg/article-inline_image-shrink_1000_1488/0/1568008495046?e=1682553600&v=beta&t=Kq8e2VD49_bLKYzrBVZpdg2lNk0IZGV5uqte8j9he_Y)

* __Requirement gathering and analysis__ - All requirements of the system to be developed are documented in a requirement specification document (PRD).
* __System Design__ - The requirement specifications from first phase are studied in this phase and the system design is prepared. This system design helps in specifying hardware and system requirements and helps in defining the overall system architecture (SRS).
* __Implementation__ - With inputs from the system design, the system is first developed in small programs called units, which are integrated in the next phase. Each unit is developed and tested for its functionality, which is referred to as Unit Testing.
* __Integration and Testing__ - All the units developed in the implmentation phase are integrated into a system after testing of each unit. Post integration the entire system is tested for any faults and failures.
* __Deployment of system__ - Once the functional and non-functional testing is done, the product is deployed  in the customer environment or released into the market.
* __Maintenance__ - There are some issues which come up in the client environment. To fix those issues, patches, are released. Also to enhance the product, some better versions are released. Maintenance is done to deliver these changes in the customer environment.

### Agile Pros and Cons
##### Pros
* Enforces discipline at each stage
* Has a defined start and end
* Progress can be easily identified
* Emphasis on requirements before code is written, means no wasted time and can improve quality

##### Cons
* Do not always know what they want
* Estimation of time and cost are different
* What is requested cannot always be created
* Division of labour is not realistic

### Agile Manifesto

The Agile Manifesto is a document that sets out the key values and principles behind the Agile philosophy and serves to help development teams work more efficiently and sustainably.

##### 4 Values
* __Individual and interactions__ over processes and tools
* __Working software__ over comprehensive documentation
* __Customer collaboration__ over contact negotiation
* __Responding to change__ over following plan

##### 12 Principles
* Our highest priority is to satisfy the customer through early and continuous deliver of value software
* Welcome changing requirements, even late in development
* Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale
* Business people and developer must work together daily throughout the project
* Build projects around motivated individuals. Give them the environment and support their need, and trust them to get the job done.
* The most efficient and effective method of conveying information to and within a developement team is face to facce information
* Working software is the primary measure of progress
* Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
* Continuous attention to technical excellence and good design enhances agility
* Simplicity - the art of maximising the amount of work not done

### Scrum Framwork

Scrum is a team based framework to develop complex systems and products.

![scrum framework](https://cdn.discordapp.com/attachments/955109188609114135/1078372002513039520/image.png)

##### Scrum Roles
* Product owner: Key stakeholder who should have deep understanding of the product and communicates with both the team and other stakeholders
* Scrum master: Ensures the team keeps to the values of Scrum, facilitates meetings and removes impediments
* Development team: 3-9 people deciding how the work would be done, everyone is accountable for the team's productivity

##### Scrum Methodology (Also known as 3 Pillars)
* Transparency: Teams work in an environment where everyone is aware of the challenges that others might be experiencing. Regular face to face conversations between cross-functional team members and project owners prevent miscommunication and information bottlenecks.
* Reflection: Frequent reflection point are built into the framework to allow team members to review their progress. Project managers use insights from these review meetings for estimation and future planning. As a result, projects can run more efficiently, wihtin budget, and on schedule.
* Adaption: Team members can reprioritise tasks based on changing customer requirements. They decide which tasks to complete first and which to revisit in the future.
* Scrum values for project teams: Scrum team follow 5 core values.

###### Core Values (Ideal Scrum Team)
* Co-located
* Engaged with customers
* Self Organising
* Accountable and Empowered
* Cross Functional

##### Scrum Artifacts
* Product Backlog: The product backlog is a dynamic list of features, requirements, enhancements, and fixes that must be completed for project success. It is essentially the team's to-do list, which is constantly revisited and reprioritised to adapt to market changes. The product owner maintains and updates the list, removing irrelevant items or adding new requests from customers.
* Sprint Backlog: The sprint backlog is the list of items to be completed by the development team in the current Sprint cycle. Before each Sprint, the team chooses which items it will work on from the product backlog. A sprint backlog is flexible and can evolve during a sprint.
* Increment: The increment is a step towards a goal or vision. It is the usable end product from a sprint. Teams can adopt different methods to define and demonstrate their spirit goals. Despite the flexibility, the fundamental sprint goal is what the team wants to achieve from the current sprint which cannot be compromised.

##### Scrum events
* Sprint Planning: In this event, the team estimates the work to be completed in the next Sprint. Members define sprint goals that are specific, measurable, and attainable. At the end of the planning meeting, every scrum member knows how each increment can be delivered in the sprint.
* Sprint: A sprint is the actual time period when the scrum team works together to finish an increment. This may take 2 - 4 weeks.
* Daily Scrum or stand up: A daily scrum is a short meeting in which team members check in and plan for the day. They report on work completed and voice any challenges in meeting sprint goals.
* Sprint Review: At the end of the spirit, the team gets together for an informal session to review the work completed and showcase it to stakeholders. The product owner might also rework the product backlog based on the current sprint.
* Sprint Retrospective: The team comes together to document and discuss what worked and what did not work during the sprint. Ideas generated are used to improve future sprints.

##### Benefits of Agile Testing
* Early and continuous feedback
* Flexibility and Adaptability
* Collaborative approach
* More Test Cycles
* Better Communication

##### User Stories
![User Story Terminology](https://cdn.discordapp.com/attachments/955109188609114135/1078383445232861254/image.png)

1. As a "type of user",
2. I want "goal",
3. so that "reason".

###### How to write good User Stories
* User comes first
* Use personas
* Create collaboratively 
* Keep your stories simple
* Start with Epics
* Refine stories until they are ready
* Add acceptance criteria
* Use paper cards
* Keep them visible

###### INVEST criteria for good User Stories
* Independent: The story is not dependent on other stories getting done.
* Negotiable: The story prompts but does not prescribe a solution.
* Valuable: The story makes clear the benefit it delivers the users.
* Estimable: The story gives the development team enough detail to estimate the size of the story.
* Small: The story is the smallest piece of work that will deliver useful software.
* Testable: The story is clear enough that you can access if the story is done.

###### The 3 C's
* Card
* Conversation
* Confirmation

##### Gherkin Example
1. __Scenario__: User clicks the link
2. __Given__: I am on the homepage
3. __When__: I click the provided link
4. __Then__: I should see the link click confirmation
