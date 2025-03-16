What are parts of hexagonal architecture?
- internal / business logic
    - entities 
    - repositories - ports allow plugging adapters into domain, e.g repostiory interface for getting an article
    - interactors
- external
   - data sources (adapters) - implement repository interfaces (e.g external APIs)
   - transport layer- input to system that triggers interactor (e.g REST controllers, cron jobs, CLI. events)
What are entities?
- Domain objects
- Not dependent on their storage

What are repositories?
- interfaces for changes to the domain object storage (CRUD)

What are interactors?
- classes that orcherstrate and perform domain actions (like Services / Use cases)
- implement business rules / validations

Adapters vs ports:
- adapters are implementation
- ports are interfaces
- adapters can be inbound (http request) and outbound (database/ message broker)
- port interfaces are parts of domain (they are contracts that domain guarantees)
Entities should not depend on outeer layers. Conversion should happen in outer layers using model classes as input.
