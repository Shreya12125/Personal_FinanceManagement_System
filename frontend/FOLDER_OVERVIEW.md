# Frontend Folder Overview

This document provides a high-level explanation of what each folder in the frontend directory does, summarizing their main responsibilities and features.

---

## src/app/
- **Purpose:** Contains all main pages, layouts, and route-specific UI for the application.
- **Key Folders:**
  - **auth/**: Handles user authentication (login, register, password reset).
  - **dashboard/**: Main user interface after login. Includes:
    - **analytics/**: Displays charts and spending analysis.
    - **budget-optimizer/**: UI for budget allocation and optimization.
    - **import/**: Interface for importing/exporting user data (e.g., transactions).
    - **insights/**: Shows AI agent insights and recommendations.
    - **ml-analytics/**: ML-powered analytics and anomaly detection.
    - **transactions/**: Transaction management (list, filter, add, edit).
      - **new/**: Form for adding new transactions.
  - **ai-assistant/**: Chatbot interface for interacting with the AI assistant.
- **Main Files:**
  - **layout.tsx**: Root layout, wraps all pages, provides global context and structure.
  - **page.tsx**: Entry point, redirects based on authentication.
  - **globals.css**: Global styles and Tailwind integration.

---

## src/components/
- **Purpose:** Contains all reusable UI components used throughout the app.
- **Examples:**
  - **Sidebar.tsx**: Sidebar navigation.
  - **MainContent.tsx**: Main content wrapper.
  - **ChatWidget.tsx**: Floating AI chat interface.
  - **ErrorBoundary.tsx**: Error handling UI.
  - **Button.tsx, Input.tsx, Navbar.tsx, ProtectedRoute.tsx, ThemeToggle.tsx**: Common UI elements.

---

## src/context/
- **Purpose:** Provides React Context for global state management.
- **Files:**
  - **AuthContext.tsx**: Authentication state and methods.
  - **SidebarContext.tsx**: Sidebar open/close state.
  - **ThemeContext.tsx**: Dark/light mode state.
  - **ToastContext.tsx**: Notification/toast functionality.

---

## src/services/
- **Purpose:** API integration layer. Handles communication with backend and ML service.
- **Files:**
  - **api.ts**: Axios instance setup, token refresh.
  - **auth.ts, agent.ts, ai.ts, budget.ts, goal.ts, insightsCache.ts, ml.ts, transaction.ts**: API calls for respective features.

---

## src/types/
- **Purpose:** TypeScript type definitions for data models, props, and API responses.
- **Files:**
  - **index.ts**: Interfaces for User, Transaction, TransactionStats, etc.

---

## Other Root Files
- **next.config.js**: Next.js configuration.
- **tsconfig.json**: TypeScript configuration.
- **tailwind.config.ts**: Tailwind CSS theme and color customization.
- **package.json**: Project metadata, dependencies, scripts.
- **postcss.config.js**: PostCSS configuration.
- **next-env.d.ts**: TypeScript environment definitions.

---

This overview helps quickly understand the purpose and main features of each folder in the frontend codebase.

---

## Features Explained

### 1. User Authentication
- Allows users to register, log in, and manage their accounts securely.
- Ensures only authorized users access their financial data.

### 2. Transaction Management
- Users can add, edit, delete, and view their financial transactions.
- Supports categorization, filtering, and anomaly detection for each transaction.

### 3. Budgeting
- Users set monthly budgets and track their spending against them.
- Visualizes budget progress and alerts users when they exceed limits.

### 4. Goal Setting
- Users define financial goals (e.g., saving for a trip) and monitor progress.
- Calculates probability of achieving goals based on spending and savings.

### 5. Analytics & Visualization
- Provides charts and summaries of income, expenses, and spending patterns.
- Helps users understand their financial habits and trends.

### 6. AI Insights & Recommendations
- Delivers personalized financial advice and anomaly alerts using AI agents.
- Users receive actionable suggestions to improve their financial health.

### 7. Data Import/Export
- Users can import transaction data from external sources (e.g., CSV).
- Export data for backup or analysis in other tools.

### 8. Category Management
- Users create, edit, and organize transaction categories.
- Enables custom categorization for more accurate tracking.

### 9. AI Chat Assistant
- Interactive chatbot for financial queries and advice.
- Uses LLM to answer questions and provide tailored recommendations.

### 10. Budget Optimization
- Computes optimal allocation of income to expenses and savings goals.
- Uses mathematical models to maximize goal achievement.

---

Each feature is designed to help users manage, analyze, and optimize their finances with ease and intelligence.
