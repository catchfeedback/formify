Certainly! Here's the complete README for your React Material-UI Form Renderer library, with the "Usage" and "Props" sections combined in the same file for ease of access:

---

```markdown
# React Material-UI Form Renderer Library

## Description

This React library provides a robust solution for rendering forms using Material-UI components.
It simplifies the creation and management of complex forms, including support for multi-step processes and dynamic form submissions.
The library handles form state, validation, and submission, making it ideal for applications requiring detailed form interactions.

## Features

- **Material-UI Form Integration**: Utilize Material-UI components for form inputs.
- **Dynamic Form Submission**: Handles submissions based on the type and state of each form question, including multi-step processes.
- **State Management**: Manages form state, including tracking of multi-step question progress.
- **Configurable Endpoints**: Allows specifying endpoints for form submissions, supporting dynamic and multi-step submissions.

## Installation

```bash
npm install @catchfeedback/formify
```

## Usage

```jsx
import { FormRenderer } from 'your-library-name';

function MyForm() {
  return (
    <FormRenderer
      questions={/* Array of questions */}
      formData={/* Initial form data */}
      endpointConfig={/* Endpoint configuration */}
      onSubmit={/* Function to call on form submission */}
      // ... other props
    />
  );
}
```

## Props

### `FormRendererProps`

- `questions: FormQuestions`: Array of form questions.
- `formData: FormData`: Initial form data.
- `endpointConfig: EndpointConfig`: Configuration for the submission endpoint.
- `onSubmit: (data: FormData) => void`: Function called when the form is submitted.
- `customSave?: (formData: FormData, endpointConfig: EndpointConfig) => Promise<any>`: Optional custom logic for saving data.
- `onSuccess?: (response: any) => void`: Optional handler for successful submission.
- `onFailure?: (error: Error) => void`: Optional handler for submission failure.

## Development Workflow

### Setup for Development

1. **Clone the Repository**: Clone the library repository to your local machine.

2. **Install Dependencies**: Navigate to the library directory and run `npm install`.

### Linking for Local Testing

1. **Link the Library**: In the library directory, run `npm link` to create a global symlink.

2. **Link in Host Application**: In your host application directory, run `npm link @catchfeedback/formify`.

### Running in Watch Mode

- In the library directory, run `npm run watch` to start the build tool in watch mode. The library will rebuild automatically on code changes.

### Testing the Library

- Make changes to the library and observe them in the host application. You may need to refresh the host application if Hot Module Replacement is not configured.

### Unlinking

- Once done, you can unlink the library by running `npm unlink your-library-name` in your host application and `npm unlink` in the library directory.

## Building for Production

Run the following command to build the library for production:

```bash
npm run build
```

## Contributing

Please read our contributing guidelines to learn about our development process, how to propose bugfixes and improvements, and how to build and test your changes to the library.
