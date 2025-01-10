
# Learning Resources App

This app helps users manage learning resources by allowing them to add, view, and delete items. It is built using Vue.js and modular components for reusability and maintainability.


## Features

- Add New Resources: Input a title, description, and link to add a new resource.
- View Stored Resources: Display a list of all saved resources with options to navigate to the links or delete them.
- Interactive UI: Provides a clean and responsive interface using reusable components.


## Components

1. BaseDialog.vue
A dialog component for displaying modal messages.

### Props:
- ```title```: The title of the dialog (optional).
### Slots:
- ```header```: Custom header content.
- ```Default```: Main content area.
- ```actions```: Action buttons for the dialog.
### Events:
- ```close```: Triggered when the dialog is closed.

2. BaseButton.vue
A reusable button component with customizable modes.

Props:
- ```type```: The button type (optional).
- ```mode```: The button mode (```flat``` for a flat-style button).

3. BaseCard.vue
A container for displaying content with a card layout.

- Slots: Default slot for card content.

4. AddResource.vue
A form for adding new learning resources.

### Features:
- Input fields for title, description, and link.
- Validates input fields to ensure non-empty values.
- Shows a dialog if validation fails.
### Injects:
```addResource```: A method for adding resources.

5. LearningResource.vue
Displays individual resources with details and actions.

### Props:
- ```id```: Unique identifier for the resource.
- ```title```: Resource title.
- ```description```: Resource description.
- ```link```: URL for the resource.
### Injects:
- ```deleteResource```: A method for deleting resources.

6. StoredResources.vue
Lists all stored resources using the LearningResource component.

### Injects:
```resources```: A list of stored resources.

7. TheResources.vue
Main component for managing the resources tab.

### Features:
- Two tabs: "Stored Resources" and "Add Resource."
- Keeps state of resources and updates them dynamically.
- Provides methods for adding and removing resources.

8. TheHeader.vue
A simple header displaying the app title.

### Props:
- ```title```: The title to display in the header.
## Project Setup

### Installation
1. Clone the repository.
2. Navigate to the project directory.
3. Install dependencies:
```npm install```

### Running the App
Start the development server:

```npm run serve```

The app will be available at http://localhost:8080.

### Building for Production
Generate the production build:

```npm run build```
## Usage/Examples

1. Launch the app in your browser.
2. Use the "Add Resource" tab to create new resources.
3. View and manage resources in the "Stored Resources" tab.


## License

This project is open-source and available under the [MIT License](https://choosealicense.com/licenses/mit/).


