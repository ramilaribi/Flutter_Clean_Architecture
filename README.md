## Core 

### Overview

The **Core Layer** is a fundamental component of our Flutter Clean Architecture project. It is designed to encapsulate the essential functionalities required for the application to operate efficiently. This layer is responsible for managing network connectivity, API interactions, error handling, and data caching. By adhering to Clean Architecture principles, the Core Layer ensures a clear separation of concerns, making the codebase more maintainable and scalable.

## Key Components

### 1. Connection

The Core Layer includes a network connectivity management system that checks for active internet connections. This functionality is crucial for ensuring that the application can make network requests only when there is a reliable connection, improving the user experience.

## 2. Databases
### API
This layer defines a robust API consumption mechanism. It abstracts the complexities of making HTTP requests, providing a simplified interface for interaction with the server. The API consumer handles various types of requests, including GET, POST, PATCH, and DELETE, allowing for flexible data retrieval and submission.
### Cache
Data caching is another essential feature of the Core Layer. It leverages local storage solutions, such as `SharedPreferences`, to persist important data across application sessions. This functionality allows the application to retain user preferences and other critical information, ensuring a seamless user experience.

### Errors
The Core Layer implements a comprehensive error-handling strategy. Custom exceptions are defined to manage different error scenarios that may occur during API interactions. This systematic approach enables the application to respond effectively to errors, enhancing reliability and user trust.

### Params
To facilitate structured data handling, the Core Layer includes specific parameter classes that encapsulate the parameters required for API requests. These classes improve code readability and maintainability, making it easier for developers to manage and pass necessary data during network interactions.

## Conclusion

The Core Layer is designed to provide a solid foundation for the application, ensuring that essential functionalities are handled efficiently. By following Clean Architecture principles, this layer supports scalability, testability, and maintainability, making it easier for developers to build upon and enhance the application in the future.
