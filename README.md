# EventSourcingExample

## Description

**EventSourcingExample** is a simple demonstration of Event Sourcing using the EventStore and Command Query Responsibility Segregation (CQRS) patterns, built using **.NET**. The project showcases how these architectural patterns can be implemented to achieve a scalable, maintainable, and highly performant system that handles complex business processes.

Event Sourcing allows us to store events (rather than current state) to model the state changes, while CQRS helps to separate the reading and writing sides of the system for better performance, scalability, and security.

## Features

- **Event Sourcing**: All state changes are stored as events in EventStore.
- **CQRS**: Commands and Queries are separated to improve system design and performance.
- **.NET-based Implementation**: Built using C# and .NET technologies for both the backend and frontend.

## Architecture Overview

This project utilizes **Event Sourcing** and **CQRS** as the core architectural patterns.

- **Event Sourcing**: The system persists all changes to the state of an entity as a sequence of events. These events are stored in **EventStore**, a purpose-built database for event storage.
- **CQRS**: The system uses two separate models:
  - **Command Model**: Responsible for handling write operations (commands).
  - **Query Model**: Responsible for handling read operations (queries), optimized for performance and scaling.

## Tech Stack

- **C#**: Primary language for backend development.
- **EventStore**: A database for storing events.
- **.NET Framework/Core**: Framework used for building and running the project.
- **HTML/CSS/JavaScript**: Used for frontend development.

## Getting Started

### Prerequisites

Before you start, ensure you have the following installed:

- .NET SDK 6.0 or later
- EventStoreDB (either local or via Docker)

### Installation

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/<your-github-username>/EventSourcingExample.git
    ```

2. Navigate to the project folder:

    ```bash
    cd EventSourcingExample
    ```

3. Install the required dependencies:

    ```bash
    dotnet restore
    ```

4. Run the application:

    ```bash
    dotnet run
    ```

The application will now be running locally. If you’re using Docker for EventStore, make sure it's running as well.

## Usage

Once the system is up and running, you can interact with it through the provided API endpoints (if any). Commands are processed asynchronously, and queries are optimized for quick retrieval of data.

### Example Scenarios:

- **Add a new event**: Trigger a command to create a new event.
- **View event history**: Use queries to retrieve the event history and current state of an entity.

## Contributing

If you’d like to contribute to this project, please follow these steps:

1. Fork this repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request with a description of your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **EventStore**: The event-sourcing database used in this project.
- **CQRS**: The Command Query Responsibility Segregation pattern for separating the read and write operations.

For more information on Event Sourcing and CQRS, check out these resources:
- [EventStore Documentation](https://eventstore.com/docs/)
- [CQRS Pattern](https://martinfowler.com/bliki/Cqrs.html)
