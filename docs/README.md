# HBnB System Architecture Documentation

## Overview
This repository contains a comprehensive technical document detailing the architecture and design of the HBnB application. The documentation includes UML diagrams that illustrate the high-level system structure, business logic, and API interaction flow.

## Table of Contents
- [Introduction](#introduction)
- [High-Level Architecture](#high-level-architecture)
- [Business Logic Layer](#business-logic-layer)
- [API Interaction Flow](#api-interaction-flow)
- [How to View Diagrams](#how-to-view-diagrams)
- [Contributing](#contributing)
- [License](#license)

## Introduction
The HBnB application is a full-stack project that implements a lodging and rental system. This documentation serves as a blueprint for the application's architecture, providing insights into the system’s design, relationships between components, and API interaction.

## High-Level Architecture
The system follows a layered architecture with three primary layers:
- **Presentation Layer:** Handles user interactions through an API.
- **Business Logic Layer:** Manages the core application logic, including users, places, reviews, and amenities.
- **Persistence Layer:** Responsible for data storage and retrieval.

### High-Level Package Diagram
The high-level package diagram visualizes the structure of the system, defining the different components and their interactions.

File: `high_level_package_diagram.md`

## Business Logic Layer
The Business Logic Layer contains the core entities of the HBnB system:
- **User:** Represents a registered user who can list places and write reviews.
- **Place:** Represents a property listed for rent.
- **Review:** A review written by a user for a place.
- **Amenity:** Represents additional services or features offered by a place.

### Business Logic Class Diagram
The class diagram defines the attributes, methods, and relationships between these entities.

File: `business_logic_class_diagram.md`

## API Interaction Flow
This section details how API calls interact with different layers of the system.

### Sequence Diagrams
- **User Registration:** Shows the process of a new user signing up.
- **Place Creation:** Displays the steps for a user to create a new listing.
- **Review Submission:** Illustrates the process of submitting a review for a place.
- **Fetching Places:** Demonstrates how the system retrieves a list of available places based on user criteria.

File: `api_sequence_diagrams.md`

## How to View Diagrams
GitHub supports Mermaid.js for rendering diagrams. To view them correctly:
1. Open the respective `.md` file in the repository.
2. Ensure that Mermaid.js syntax is correctly formatted using the fenced code block.
3. If necessary, use a Markdown preview tool that supports Mermaid.js.

## Contributing
Contributions to this documentation are welcome! If you find any inaccuracies or areas for improvement:
1. Fork the repository.
2. Create a new branch for your changes.
3. Submit a pull request with detailed explanations.

## License
This project follows the MIT License. See `LICENSE` for details.


