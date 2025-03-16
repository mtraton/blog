What are parts of hexagonal architecture?
- internal / business logic
    - entities 
    - repositories
    - interactors
- external
   - data sources (adapters) - implement repository interfaces
   - transport layer - input to system that triggers interactor (e.g REST controllers, cron jobs, CLI. events)

What are entities?
- Domain objects
- Not dependent on their storage

What are repositories?
- interfaces for changes to the domain object storage (CRUD)

What are interactors?
- classes that orcherstrate and perform domain actions (like Services / Use cases)
- implement business rules / validations

