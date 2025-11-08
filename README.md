# Code Crafted Resume Documentation

This document provides an overview of the Code Crafted Resume application, including its functionality, technical stack, project setup instructions, and key use cases.

## 1. Overview

Code Crafted Resume is a client-side resume builder specifically designed for developers and software engineers. It allows users to create and customize their resumes with features like drag-and-drop reordering of sections and list items, a live side-by-side preview, and the ability to generate and download an ATS-friendly PDF. The application prioritizes user privacy by performing all PDF generation directly in the browser, ensuring no user data is collected or shared.

## 2. Tech Stack

### Frontend

The application is built as a Single Page Application (SPA) using the following frontend technologies:

*   **React:** The core library for building the user interface.
*   **TypeScript:** Used for all new components, hooks, and utility files to enhance code quality and maintainability.
*   **Tailwind CSS:** Utilized for all styling, providing a utility-first approach for responsive and consistent design.
*   **Shadcn/ui:** A collection of reusable UI components that are integrated to maintain consistency and accelerate development.
*   **Zustand:** A lightweight state management solution for managing global application state. Data is persisted locally using `zustand/middleware/persist`.
*   **@react-pdf/renderer:** A dedicated library for generating and rendering PDF documents directly on the client-side.
*   **@dnd-kit:** A modern, lightweight, and highly customizable drag-and-drop toolkit for React, used for reordering resume sections and list items.
*   **Lucide-react:** The preferred library for all icons within the application.
*   **File-saver:** Used to enable client-side downloading of the generated PDF files.
*   **pdfjs-dist:** For rendering PDF previews within the application's UI.

### Backend

This application is entirely client-side. There is no dedicated backend server or API. All data processing and PDF generation occur within the user's browser.

### Database

There is no traditional database used. All application state, including user-entered resume data, is managed by **Zustand** and persisted in the browser's `localStorage` for a seamless user experience across sessions.

## 3. Project Setup

To set up and run the Code Crafted Resume project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd code-crafted-resume
    ```
2.  **Install dependencies:**
    The project uses `npm`. Install all required packages:
    ```bash
    npm install
    ```
    *Note: The `postinstall` script will automatically run `patch-package` to apply necessary patches for `@react-pdf/pdfkit`.*
3.  **Start the development server:**
    ```bash
    npm start
    ```
    This will start the application in development mode, and it will typically open in your browser at `http://localhost:3000`.

## 4. Use Cases

The Code Crafted Resume application is designed to address the following primary use cases:

*   **Resume Creation:** Users can easily input their personal details, work experience, projects, education, skills, and other relevant information through a guided form interface.
*   **Customization and Reordering:** Users can dynamically add, remove, and reorder resume sections (e.g., Work Experience, Projects) and bullet points within sections using intuitive drag-and-drop functionality.
*   **Live Preview:** A side-by-side live preview allows users to see real-time updates to their resume as they fill out the form, ensuring the final output matches their expectations.
*   **PDF Generation and Download:** The application generates a professional, ATS-friendly PDF version of the resume directly in the browser, which users can then download to their local machine.
*   **Sample Data Population:** For quick starts or demonstrations, users can populate the form with sample data.
*   **Data Persistence:** User data is automatically saved locally in the browser, allowing users to close and reopen the application without losing their progress.

## 5. Preview

![Fom Preview](preview.png)