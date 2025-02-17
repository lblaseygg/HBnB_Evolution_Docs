# Sequence Diagrams for API Calls

## 1. User Registration
This diagram illustrates the interaction flow when a user registers for a new account.

```mermaid
sequenceDiagram
    participant User
    participant API
    participant BusinessLogic
    participant Database

    User->>API: POST /register (User Data)
    API->>BusinessLogic: Validate user data
    BusinessLogic->>Database: Check if user already exists
    Database-->>BusinessLogic: User does not exist
    BusinessLogic->>Database: Save new user
    Database-->>BusinessLogic: User saved
    BusinessLogic-->>API: Return success response
    API-->>User: 201 Created (User Registered)
```

---

## 2. Place Creation
This diagram shows how a user creates a new place listing.

```mermaid
sequenceDiagram
    participant User
    participant API
    participant BusinessLogic
    participant Database

    User->>API: POST /places (Place Data)
    API->>BusinessLogic: Validate place data
    BusinessLogic->>Database: Save new place
    Database-->>BusinessLogic: Place saved
    BusinessLogic-->>API: Return success response
    API-->>User: 201 Created (Place Registered)
```

---

## 3. Review Submission
This diagram represents the process when a user submits a review for a place.

```mermaid
sequenceDiagram
    participant User
    participant API
    participant BusinessLogic
    participant Database

    User->>API: POST /reviews (Review Data)
    API->>BusinessLogic: Validate review data
    BusinessLogic->>Database: Save review
    Database-->>BusinessLogic: Review saved
    BusinessLogic-->>API: Return success response
    API-->>User: 201 Created (Review Submitted)
```

---

## 4. Fetching a List of Places
This diagram shows the process of retrieving a list of places based on filters.

```mermaid
sequenceDiagram
    participant User
    participant API
    participant BusinessLogic
    participant Database

    User->>API: GET /places?filter=criteria
    API->>BusinessLogic: Process filter parameters
    BusinessLogic->>Database: Fetch filtered places
    Database-->>BusinessLogic: Return list of places
    BusinessLogic-->>API: Format response
    API-->>User: 200 OK (List of Places)
```

---

## Explanatory Notes
### 1. **User Registration**
- The API receives user data and validates it.
- The Business Logic checks if the user already exists before saving.
- If the user is new, they are saved in the database, and a success response is returned.

### 2. **Place Creation**
- The API receives place details and validates them.
- The Business Logic ensures all required data is provided.
- The new place is saved in the database, and a success response is returned.

### 3. **Review Submission**
- The API processes a user’s review request.
- The Business Logic ensures the review is valid and saves it to the database.
- A success response is returned to the user.

### 4. **Fetching a List of Places**
- The API handles user requests with filters.
- The Business Logic processes filters and queries the database.
- The database returns a list of places, which is formatted and sent back to the user.

These sequence diagrams provide a **clear view** of how different layers interact in handling API requests.

