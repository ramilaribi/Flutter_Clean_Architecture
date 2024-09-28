<h1 align="center">Flutter Clean Architecture</h1>

<p align="center">
    <img src="assets/your-image.png" alt="Description of image" width="300"/>
</p>

The **Flutter Clean Architecture** project is designed to provide a robust and scalable structure for Flutter applications. By adhering to Clean Architecture principles, this project separates concerns across different layers, making the codebase maintainable, testable, and extensible.

---

## Core Layer 🛠️

The **Core Layer** is a fundamental component that encapsulates essential functionalities required for the application, such as network management, API interactions, error handling, and data caching. 

### Key Components

#### 1. Connection 🌐

Manages network connectivity, ensuring reliable internet connections for network requests.

- **NetworkInfo**: An abstract class that provides a contract for network connectivity checks.
- **NetworkInfoImpl**: Implements the `NetworkInfo` interface using the `DataConnectionChecker` package.

#### 2. Databases 🗄️

- **API**: Abstracts the complexities of making HTTP requests.
- **Cache**: Implements data caching using local storage solutions (e.g., `SharedPreferences`).

#### 3. Errors ❗

Establishes a comprehensive error-handling strategy by defining custom exceptions.

- **ErrorModel**: Encapsulates error details, including HTTP status codes and error messages.
- **ServerException**: Captures server-related errors with detailed context.
- **CacheException**: Represents exceptions that occur during caching operations.

#### 4. Params 📦

Includes parameter classes for API requests.

- **TemplateParams**: Represents a unique identifier for a template.
- **UserParams**: Represents a unique identifier for a user.
- **PostParams**: Represents a unique identifier for a post.

---

## Presentation Layer 🎨

The **Presentation Layer** is responsible for displaying data to the user and handling user interactions. It serves as the UI component of the application, ensuring that the user experience is intuitive and responsive.

#### 1. UI Widgets 📱

- **Screens**: Represent the various views of the application, each corresponding to a different feature or section.
- **Widgets**: Reusable components that make up the UI, promoting consistency and reusability across the application.

#### 2. State Management 📊

Utilizes state management solutions (e.g., Provider, Riverpod) to manage the application state efficiently, ensuring that the UI reflects changes in data seamlessly.

---

## Domain Layer 🏗️

The **Domain Layer** contains the business logic of the application. It defines the core use cases and entities, providing an interface for the other layers to interact with.

#### 1. Entities 🧑‍🤝‍🧑

- **User**: Represents a user within the application, containing relevant attributes such as name, email, and id.
- **Post**: Represents a post created by a user, containing attributes like content, timestamp, and id.

#### 2. Repositories 🏪

- **UserRepository**: Defines methods for accessing user-related data, such as creating, updating, and fetching users.
- **PostRepository**: Defines methods for accessing post-related data, including creating, updating, and fetching posts.

#### 3. Use Cases 📋

Defines the various actions that can be performed within the application, such as creating a user, fetching posts, and updating user profiles. Each use case corresponds to a specific business requirement.

---

## Data Layer 📥

The **Data Layer** is responsible for managing data sources, including local databases and remote APIs. It handles data retrieval, storage, and mapping to domain entities.

#### 1. Models 🏷️

- **UserModel**: Represents the user data structure used to map API responses to the domain `User` entity.
- **PostModel**: Represents the post data structure used to map API responses to the domain `Post` entity.

#### 2. Repositories 🏪

- **UserRepository**: Defines methods for accessing user-related data.
- **PostRepository**: Defines methods for accessing post-related data.

#### 3. Data Sources 🗃️

- **Remote Data Source**: Handles API interactions to fetch data from external servers.
- **Local Data Source**: Manages local data storage (e.g., SQLite, SharedPreferences) to persist information.

---

## Template for Entities 📝

This project includes a **template** for entities that you can easily customize to fit your specific requirements. By using these templates, you can save time and streamline your development process. Feel free to replace the existing entities with your own to accelerate your application development!

---

## Conclusion 🎉

The **Flutter Clean Architecture** provides a solid foundation for building scalable and maintainable applications. By clearly separating concerns across the Core, Presentation, Domain, and Data layers, developers can enhance the application easily in the future while ensuring a robust and reliable user experience.

---
Feel free to ask for help! 🤝 Just don’t be surprised if I ask if you’ve tried turning it off and on again—every developer’s favorite solution! 😂🔄💻
