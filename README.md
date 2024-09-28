## Core Layer Documentation

### Overview

The **Core Layer** is a fundamental component of our Flutter Clean Architecture project. It encapsulates essential functionalities required for the application, such as network management, API interactions, error handling, and data caching. This layer adheres to Clean Architecture principles, ensuring a clear separation of concerns for better maintainability and scalability.

### Key Components

#### 1. Connection

**File**: `network_info.dart`

Manages network connectivity, ensuring that the application can make network requests only when a reliable internet connection is available. This enhances the overall user experience. The following classes are defined:

- **NetworkInfo**: An abstract class that provides a contract for network connectivity checks. It includes a getter, `isConnected`, which returns a `Future<bool>` indicating the network connection status.

- **NetworkInfoImpl**: Implements the `NetworkInfo` interface using the `DataConnectionChecker` package. It uses `hasConnection` to determine the current network status, returning a boolean value asynchronously.

#### 2. Databases

- **API**: Facilitates API consumption by abstracting the complexities of making HTTP requests. It provides a simplified interface for various request types (GET, POST, PATCH, DELETE) to interact with the server effectively.
  
- **Cache**: Implements data caching using local storage solutions (e.g., `SharedPreferences`) to persist critical information and user preferences across sessions, promoting a seamless user experience.

#### 3. Errors

Establishes a comprehensive error-handling strategy by defining custom exceptions for different scenarios that may occur during API interactions. This approach improves application reliability and user trust. The following custom exceptions are defined:

- **ErrorModel**: This class encapsulates the error details, including the HTTP status code and error message. It provides a structured way to represent error information received from API responses.

- **ServerException**: A base exception class that captures server-related errors. It includes an instance of `ErrorModel` to provide detailed error context.

- **CacheException**: Represents exceptions that occur during caching operations, encapsulating an error message for clarity.

Additionally, specific server exceptions extend `ServerException` to handle various types of errors, such as:
- **ConnectionTimeoutException**: Triggered when a connection request times out.
- **UnauthorizedException**: Indicates that the user is not authorized to access the requested resource.
- **NotFoundException**: Represents a 404 error when the requested resource cannot be found.

#### 4. Params

**File**: `params.dart`

Includes parameter classes that encapsulate the parameters required for API requests. This structured approach enhances code readability and maintainability, making it easier to manage and pass data during network interactions. The following parameter classes are defined:

- **TemplateParams**: Contains the `id` parameter, representing a unique identifier for a template.

- **UserParams**: Contains the `id` parameter, representing a unique identifier for a user.

- **PostParams**: Contains the `id` parameter, representing a unique identifier for a post.

### Conclusion

The Core Layer provides a solid foundation for the application, ensuring efficient handling of essential functionalities. By following Clean Architecture principles, this layer supports scalability, testability, and maintainability, allowing developers to enhance the application easily in the future.
