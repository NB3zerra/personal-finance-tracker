# **Personal Finance Tracker**

![Personal Finance Tracker Logo](docs/logo.png) <!-- Add a logo if available -->

## **Overview**
The **Personal Finance Tracker** is a web and mobile application designed to help users manage their finances efficiently. With features like expense tracking, budget management, and data visualization, this app is a comprehensive tool for personal financial planning.

The project is modular, with separate submodules for the backend, frontend, and mobile applications, ensuring scalability and maintainability.

---

## **Features**
- **Expense Tracking**: Add, edit, and categorize your expenses effortlessly.
- **Budget Management**: Set monthly budgets and track your spending progress.
- **Data Visualization**: View spending trends with interactive charts and graphs.
- **Mobile Access**: Manage your finances on the go with the React Native mobile app.
- **Secure Authentication**: Protect your data with token-based authentication.

---

## **Tech Stack**
| Component     | Technology                                   |
|---------------|---------------------------------------------|
| **Backend**   | C# .NET 8, Entity Framework, Azure App Services |
| **Frontend**  | React, Chart.js/D3.js, Azure Static Web Apps |
| **Mobile**    | React Native, Expo                          |
| **DevOps**    | Azure DevOps, Azure CI/CD Pipelines         |
| **Database**  | Azure SQL Database                         |

---

## **Repository Structure**
The project is organized into multiple submodules for clear separation of concerns:

```
personal-finance-tracker/
├── backend/                     # C# .NET 8 API (Submodule)
├── frontend/                    # React Web App (Submodule)
├── mobile/                      # React Native Mobile App (Submodule)
├── shared/                      # Shared Code or Resources (Optional Submodule)
├── docs/                        # Documentation (API specs, architecture, etc.)
├── ci-cd/                       # Azure CI/CD Configuration
├── README.md                    # Overview of the project
├── .gitmodules                  # Git submodules configuration
```

Each submodule is maintained in its own repository:
- [Backend](https://github.com/<your-org>/personal-finance-tracker-backend)
- [Frontend](https://github.com/<your-org>/personal-finance-tracker-frontend)
- [Mobile](https://github.com/<your-org>/personal-finance-tracker-mobile)
- [Shared](https://github.com/<your-org>/personal-finance-tracker-shared) *(optional)*

---

## **Getting Started**

### **Prerequisites**
- Git
- Node.js and npm (for frontend and mobile)
- .NET SDK (for backend)
- Azure CLI (for deployment)

### **Clone the Repository**
Clone the main repository and initialize submodules:
```bash
git clone --recurse-submodules https://github.com/<your-org>/personal-finance-tracker.git
cd personal-finance-tracker
```

If you've already cloned the repository without submodules, initialize them manually:
```bash
git submodule update --init --recursive
```

### **Backend Setup**
1. Navigate to the `backend/` directory:
   ```bash
   cd backend
   ```
2. Restore dependencies and run the project:
   ```bash
   dotnet restore
   dotnet run
   ```
3. The backend API will be available at `http://localhost:5000`.

### **Frontend Setup**
1. Navigate to the `frontend/` directory:
   ```bash
   cd frontend
   ```
2. Install dependencies and start the development server:
   ```bash
   npm install
   npm start
   ```
3. The frontend app will be available at `http://localhost:3000`.

### **Mobile Setup**
1. Navigate to the `mobile/` directory:
   ```bash
   cd mobile
   ```
2. Install dependencies and start the Expo server:
   ```bash
   npm install
   npm start
   ```
3. Use the Expo Go app on your mobile device to scan the QR code and test the app.

---

## **Contributing**
We welcome contributions from the community! To get started:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes and push to your fork.
4. Submit a pull request to the main repository.

---

## **CI/CD Pipeline**
This project uses Azure DevOps pipelines for continuous integration and deployment:
- **Backend**: Deployed to Azure App Services.
- **Frontend**: Deployed to Azure Static Web Apps.
- **Mobile**: Expo builds for Android and iOS.

Pipeline configurations are located in the `ci-cd/` folder.

---

## **License**
This project is licensed under the [MIT License](LICENSE).

---

## **Contact**
For questions or feedback, feel free to contact:
- **Project Maintainer**: [Your Name](mailto:your-email@example.com)
- **Organization**: [Your Organization](https://your-organization.com)