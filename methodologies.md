# Methodologies

### Describe KISS principle?
Keep it simple stupid

### Describe basics of DDD?
https://docs.microsoft.com/en-us/archive/msdn-magazine/2009/february/best-practice-an-introduction-to-domain-driven-design

### Describe basics of grasp?
General Responsibility Assignment Software Patterns (or Principles), abbreviated GRASP, is a set of "nine fundamental principles in object design and responsibility assignment" 

The different patterns and principles used in GRASP are controller, creator, indirection, information expert, low coupling, high cohesion, polymorphism, protected variations, and pure fabrication.[2] All these patterns solve some software problem common to many software development projects. These techniques have not been invented to create new ways of working, but to better document and standardize old, tried-and-tested programming principles in object-oriented design.

### Describe Continious Delivery?

Continuous delivery (CD) is a software engineering approach in which teams produce software in short cycles, ensuring that the software can be reliably released at any time and, when releasing the software, without doing so manually.[1][2] It aims at building, testing, and releasing software with greater speed and frequency. The approach helps reduce the cost, time, and risk of delivering changes by allowing for more incremental updates to applications in production. A straightforward and repeatable deployment process is important for continuous delivery.

CD contrasts with continuous deployment, a similar approach in which software is also produced in short cycles but through automated deployments rather than manual ones.


### Describe Continuous Integration ?

Continuous integration (CI) is the practice of developers regularly integrating their code changes into a repository. Integration may take place several times a day and is verified by automated tests and a build process. As a result, integration challenges can be avoided, bugs can be found early in the development cycle, fixed, and tested iteratively. Every time new commits are integrated into the main branch, continuous integration emphasizes testing automation to make sure the application is not broken.


### What is GDPR? Name 3 things how to became GDPR compliant?
What is the GDPR? Europe’s new data privacy and security law includes hundreds of pages’ worth of new requirements for organizations around the world. This GDPR overview will help you understand the law and determine what parts of it apply to you.
https://gdpr.eu/what-is-gdpr/


### Describe YAGNI principle?
You aren't gonna need it
is a principle of extreme programming (XP) that states a programmer should not add functionality until deemed necessary.

### Describe DRY
Do not repeat yourself - is a principle of software development aimed at reducing repetition of software patterns,[1] replacing it with abstractions or using data normalization to avoid redundancy

### Describe what is Agile Method?
A sprint is a period of time allocated for a particular phase of a project. Sprints are considered to be complete when the time period expires. There may be disagreements among the members of the team as to whether or not the development is satisfactory; however, there will be no more work on that particular phase of the project. The remaining phases of the project will continue to develop within their respective time frames.

The general principles of the Agile Method
- Satisfy the client and continually develop software.
- Changing requirements are embraced for the client’s competitive advantage.
- Concentrate on delivering working software frequently. Delivery preference will be placed on the shortest possible time span.
- Developers and business people must work together throughout the entire project.
- Projects must be based on people who are motivated. Give them the proper environment and the support that they need. - They should be trusted to get their jobs done.
- Face-to-face communication is the best way to transfer information to and from a team.
- Working software is the primary measurement of progress.
- Agile processes will promote development that is sustainable. Sponsors, developers, and users should be able to maintain an indefinite, constant pace.
- Constant attention to technical excellence and good design will enhance agility.
- Simplicity is considered to be the art of maximizing the work that is not done, and it is essential.
- Self-organized teams usually create the best designs.
- At regular intervals, the team will reflect on how to become more effective, and they will tune and adjust their behavior accordingly.

### Describe Scrum?
Agile Scrum Methodology
Scrum is a lightweight Agile project management framework that can be used to manage iterative and incremental projects of all types

In Scrum we are divide Each Phase on Development on Sprints.
If some not done we are put in Backlog.
And do in the next sprint.

### Describe Kanban?
Kanban is a highly visual workflow management method that is popular among Lean teams. In fact, 83% of teams practicing Lean use Kanban to visualize and actively manage the creation of products with an emphasis on continual delivery, while not overburdening the development team. Like Scrum, Kanban is a process designed to help teams work together more effectively.

Kanban is based on 3 basic principles:

- Visualize what you’ll do today (workflow): Seeing all the items within the context of each other can be very informative
- Limit the amount of work in progress (WIP): This helps balance the flow-based approach so teams don‘t start and commit to too much work at once
- Enhance flow: When something is finished, the next highest priority item from the backlog is pulled into play
Kanban promotes continuous collaboration and encourages active, ongoing learning and improvement by defining the best possible team workflow.

For example in board with lists:
- TODO
- DOING
- DONE

### Describe Software Development Life Cycle (SDLC)?

Software Development Life Cycle (SDLC) is a process used by the software industry to design, develop and test high quality softwares. The SDLC aims to produce a high-quality software that meets or exceeds customer expectations, reaches completion within times and cost estimates.

Stage 1: Planning and Requirement Analysis
Requirement analysis is the most important and fundamental stage in SDLC. It is performed by the senior members of the team with inputs from the customer, the sales department, market surveys and domain experts in the industry. 

Stage 2: Defining Requirements
Once the requirement analysis is done the next step is to clearly define and document the product requirements and get them approved from the customer or the market analysts. This is done through an SRS (Software Requirement Specification) document which consists of all the product requirements to be designed and developed during the project life cycle.

Stage 3: Designing the Product Architecture
SRS is the reference for product architects to come out with the best architecture for the product to be developed. Based on the requirements specified in SRS, usually more than one design approach for the product architecture is proposed and documented in a DDS - Design Document Specification.

Stage 4: Building or Developing the Product
In this stage of SDLC the actual development starts and the product is built. The programming code is generated as per DDS during this stage. If the design is performed in a detailed and organized manner, code generation can be accomplished without much hassle.

Stage 5: Testing the Product
This stage is usually a subset of all the stages as in the modern SDLC models, the testing activities are mostly involved in all the stages of SDLC. 

Stage 6: Deployment in the Market and Maintenance
Once the product is tested and ready to be deployed it is released formally in the appropriate market. Sometimes product deployment happens in stages as per the business strategy of that organization. 

SDLC Models have 5 models of development of software is -
Waterfall Model
Iterative Model
Spiral Model
V-Model
Big Bang Model

### What is Event Sourcing?
Event Sourcing is an architectural design pattern that stores data in an append-only log. It is part of a wider ecosystem of design patterns that work together in various ways to allow developers to create the most effective architecture for their needs.

### What is CQRS?
CQRS stands for Command and Query Responsibility Segregation, a pattern that separates read and update operations for a data store. Implementing CQRS in your application can maximize its performance, scalability, and security.

- separating writes from reads
- queries only return data, free from side effects
- events handled reliably


### What Design Patterns you know?

Builder, Decorator, Form, Interactor, Observer, Policy, Presenter, Query, Service, ValueObject.




