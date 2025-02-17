classDiagram
    class PresentationLayer {
        <<Interface>>
        + ServiceAPI
    }
    
    class BusinessLogicLayer {
        + User
        + Place
        + Review
        + Amenity
        + Facade
    }
    
    class PersistenceLayer {
        + DatabaseAccess
    }

    PresentationLayer --> BusinessLogicLayer : Uses Facade
    BusinessLogicLayer --> PersistenceLayer : Handles Data Storage

