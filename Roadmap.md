# **Personal Finance Tracker - Roadmap**

This roadmap outlines the development process for the **Personal Finance Tracker**, considering the use of submodules for backend, frontend, mobile, and shared components.

---

## **Phase 1: Project Setup**
**Goal**: Create the foundation for the project with all submodules and repositories integrated.

1. **Main Repository Setup**
   - Create a new repository: `personal-finance-tracker` (main repo).
   - Add submodules for each component:
     - `backend/` (C# .NET 8 API)
     - `frontend/` (React web app)
     - `mobile/` (React Native app)
     - `shared/` (Optional: shared utilities/constants)
   - Initialize the `.gitmodules` file and commit the submodule structure.

2. **Submodule Repositories**
   - Create separate repositories for:
     - `personal-finance-tracker-backend`
     - `personal-finance-tracker-frontend`
     - `personal-finance-tracker-mobile`
     - `personal-finance-tracker-shared` (optional)
   - Clone each submodule into its respective directory.

3. **CI/CD Prep**
   - Create a `ci-cd/` folder in the main repository for Azure DevOps pipelines.
   - Add placeholder pipeline YAML files for backend, frontend, and mobile.

---

## **Phase 2: Backend Development**
**Goal**: Build the core API for the project.

1. **Setup the Backend**
   - Scaffold a new C# .NET 8 project in the `backend/` submodule.
   - Install and configure essential packages:
     - Entity Framework Core for database access.
     - Identity for user authentication.
     - Swagger for API documentation.
   - Design the database schema:
     - Users table.
     - Expenses table (with categories, amounts, etc.).
     - Budgets table.

2. **Implement Core Features**
   - Authentication and Authorization:
     - Register, login, and token-based authentication (JWT).
   - Expense Management:
     - CRUD operations for expenses.
     - Categorization of expenses.
   - Budget Management:
     - CRUD operations for budgets.
     - Track budget progress.

3. **Testing**
   - Write unit tests for services and controllers.
   - Set up integration tests for API endpoints.

4. **CI/CD Pipeline**
   - Create an Azure pipeline for building, testing, and deploying the backend to Azure App Services.

---

## **Phase 3: Frontend Development**
**Goal**: Develop the web dashboard for users to interact with the application.

1. **Setup the Frontend**
   - Scaffold a new React project in the `frontend/` submodule.
   - Install necessary libraries:
     - Axios for API calls.
     - React Router for navigation.
     - Chart.js or D3.js for data visualization.
   - Configure a global state management solution (e.g., Redux, Context API).

2. **Implement Core Features**
   - Authentication:
     - Login and registration pages.
     - Secure API calls with tokens.
   - Expense Dashboard:
     - Display expenses with filters (by date, category).
     - Add/Edit/Delete expenses.
   - Budget Tracker:
     - Show budgets with progress bars.
     - Visualize spending trends using charts.

3. **Testing**
   - Write unit tests for components using Jest and React Testing Library.
   - Perform end-to-end testing with tools like Cypress.

4. **CI/CD Pipeline**
   - Create an Azure pipeline for building and deploying the frontend to Azure Static Web Apps.

---

## **Phase 4: Mobile Development**
**Goal**: Build a mobile app for on-the-go expense tracking.

1. **Setup the Mobile App**
   - Scaffold a new React Native project in the `mobile/` submodule.
   - Install libraries:
     - Axios for API calls.
     - React Navigation for navigation.
   - Test on both Android and iOS simulators.

2. **Implement Core Features**
   - Authentication:
     - Login and registration screens.
     - Secure API calls with tokens.
   - Quick Expense Tracking:
     - Add expenses quickly via a mobile-friendly form.
   - Budget Overview:
     - Show budgets and expense summaries.

3. **Testing**
   - Write unit tests for components using Jest.
   - Test app functionality on real devices.

4. **CI/CD Pipeline**
   - Create an Azure pipeline for building and deploying mobile apps (Expo or APK/IPA).

---

## **Phase 5: Shared Module (Optional)**
**Goal**: Extract and centralize shared utilities or constants.

1. **Setup the Shared Module**
   - Scaffold a new project in the `shared/` submodule.
   - Add reusable components, utilities, or constants:
     - API endpoint URLs.
     - Common models (e.g., Expense, Budget).

2. **Integrate Across Submodules**
   - Add the shared module as a dependency to the backend, frontend, and mobile projects.

3. **Testing**
   - Write unit tests for shared utilities.

---

## **Phase 6: Final Integration and Deployment**
**Goal**: Fully integrate and deploy all components.

1. **End-to-End Testing**
   - Test the entire system from user authentication to data visualization.
   - Verify the mobile, web, and backend work seamlessly together.

2. **Documentation**
   - Create comprehensive documentation in the `docs/` folder:
     - API Documentation.
     - User Guide for setting up the project locally.
     - CI/CD pipeline setup instructions.

3. **Deployment**
   - Deploy the backend, frontend, and mobile app to Azure.
   - Monitor performance and logs using Azure Application Insights.

---

## **Phase 7: Post-MVP Enhancements**
**Goal**: Add advanced features to improve the project.

1. **Income Tracking**
   - Add an income management module.
2. **Savings Goals**
   - Allow users to set and track savings goals.
3. **Multi-Currency Support**
   - Enable support for different currencies.
4. **Bank Sync**
   - Integrate financial APIs (e.g., Plaid, Yodlee) to sync transactions.
5. **AI Insights**
   - Use machine learning to provide insights or suggest budgets.

---

## **Milestones**
| **Milestone**               | **Timeline** |
|-----------------------------|--------------|
| Setup Repositories & Submodules | 1 week       |
| Backend MVP Development      | 3 weeks      |
| Frontend MVP Development     | 3 weeks      |
| Mobile MVP Development       | 4 weeks      |
| Final Integration & Testing  | 2 weeks      |
| Deployment                   | 1 week       |
| Post-MVP Enhancements        | Ongoing      |