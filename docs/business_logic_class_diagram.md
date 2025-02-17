classDiagram
    class BaseModel {
        +UUID id
        +datetime created_at
        +datetime updated_at
        +save()
        +to_dict()
    }

    class User {
        +string email
        +string password
        +string first_name
        +string last_name
        +list places
        +list reviews
        +create_place()
        +add_review()
    }

    class Place {
        +UUID id
        +string name
        +string description
        +int number_rooms
        +int number_bathrooms
        +float price_per_night
        +User owner
        +list amenities
        +list reviews
        +add_amenity()
        +add_review()
    }

    class Review {
        +UUID id
        +User user
        +Place place
        +string text
        +int rating
        +update_text()
    }

    class Amenity {
        +UUID id
        +string name
    }

    BaseModel <|-- User
    BaseModel <|-- Place
    BaseModel <|-- Review
    BaseModel <|-- Amenity

    User --> Place : owns >
    User --> Review : writes >
    Place --> Review : has >
    Place --> Amenity : has >

