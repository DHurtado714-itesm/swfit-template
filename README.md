# Swift App Template

This Swift App Template is structured using Clean Architecture principles, emphasizing the use of MVVM (Model-View-ViewModel) for the presentation layer. This structure aids in creating a scalable, maintainable, and testable application.

## Architecture

Our project is organized into major layers to encapsulate the core functionalities, as described below:

- **Data:** Data persistence and network communication layer. It holds Models related to the network and database management.
- **Domain:** Contains business logic and use cases of the application.
- **Framework:** Includes the UI (View) and the presentation logic (ViewModel).

## Directory Structure

The project is divided into the following directories:

```
/SwiftAppTemplate
    /Data
        /Models
            /Network
    /Domain
    /Framework
        /View
        /ViewModel
```

### Data Layer

The Data layer is structured as follows:

- `/Data/Models` - Defines the entities used across the application, focusing on the shape of the data.
- `/Data/Models/Network` - Contains model definitions that are specific to network requests and responses.

### Domain Layer

Located under `/Domain`, this layer encapsulates the business logic of the application. It's typically framework-agnostic and can be reused within different contexts of the application.

### Framework Layer

The Framework layer is where the MVVM pattern comes into play:

- `/Framework/View` - This directory will contain all the `UIViewControllers`, custom `UIView` subclasses, and any storyboard/XIB files. Views should be dumb and delegate user interactions to the ViewModel.
- `/Framework/ViewModel` - Here, we define the `ViewModels` that hold the state of the View and its presentation logic. They act upon the Model and provide data for the Views.

## Getting Started

To use this template, you may follow these steps:

1. Populate the `/Data/Models` with your app-specific data structures, and implement network handling within `/Data/Models/Network`.
2. Utilize the `/Domain` layer to define your business logic, such as use cases or business rules.
3. In the `/Framework` layer, build your Views and ViewModels. Views should be kept as simple as possible, with ViewModels handling most of the logic.

## Contributing

We welcome contributions that help improve the structure or functionality of this template. To contribute:

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/YourFeature`).
3. Commit your Changes (`git commit -m 'Add some YourFeature'`).
4. Push to the Branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

## Conclusion

By following these architectural guidelines, you'll maintain a clean codebase and enjoy an application that's easier to scale and maintain. Thank you for choosing this Swift App Template as the foundation for your project!