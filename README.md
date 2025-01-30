# demo-rasa

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/erikamaschio/demo-rasa/HEAD)


Aqui está a versão atualizada da documentação com as instruções de acesso:  

---

# **Documentation - Vivabem+**  

## **General Project Structure**  

### **Main Technologies:**  

- **React 18 + React Router 6**  
- **Grommet (Design System)**  
- **Recharts (Charts)**  
- **Styled Components (Global Styles)**  

### **Architectural Patterns:**  

- **Modular Componentization**  
- **Clear separation between:**  
  - **Pages** (`src/pages`)  
  - **Reusable Components** (`src/components`)  
  - **Static Data** (`src/data`)  
  - **Route Configuration** (`src/router`)  

---

## **How to Run the Project**  

1. **Enter the frontend folder:**  
   ```sh
   cd frontend
   ```  
2. **Open the terminal**  
3. **Install dependencies:**  
   ```sh
   npm i
   ```  
4. **Start the application:**  
   ```sh
   npm start
   ```  
5. **The application will open in your browser.**  

---

## **Application Entry Point**  

### **index.js**  
- **Function:** React Initialization  

- **Features:**  
  - Global theme configuration (Material-UI)  
  - Essential Wrappers:  
    - **BrowserRouter** for routing  
    - **React.StrictMode** for validations  

---

### **App.jsx**  
- **Role:** Root Component  

- **Structure:**  
  - Delegates navigation to **AppRouter**  
  - Ideal point for adding:  
    - **Global Contexts** (Authentication/Theme)  
    - **Persistent Elements** (Global Header/Footer)  

---

## **Routing System**  

### **AppRouter.jsx**  

- **Main Routes:**  
```javascript
<Routes>
  <Route path="/login" element={<Login/>} />
  <Route path="/createaccount" element={<CreateAccount/>} />
  <Route path="/dashboard" element={<Dash />} />
  {/* ... other routes */}
</Routes>
```

- **Notes:**  
  - Basic navigation logic after login  
  - Default redirect to `/login`  

---

## **Main Pages**  

### **PageDashboard.jsx**  
- **Layout:**  
  - **The screen is not responsive.**  
  - Grid layout with fixed Header/Sidebar  
  - Dynamic content area (**Dashboard2**)  

- **Technologies:**  
  - **Grommet Grid System**  
  - Shared state for tab control  

---

### **CreateAccount.jsx**  

- **Key Components:**  
  - Form with visual password validation  
  - Custom hover effects  
  - Complex gradients for visual emphasis  

- **Highlights:**  
  - Custom global styles  
  - Integration with routing for login/dashboard  

---

## **Reusable Components**  

### **SidebarComponent.jsx**  
- **Functionality:**  
  - Navigation between dashboard sections  
  - Buttons with dynamic hover effects  
  - Integration with the routing system  

### **HeaderComponent.jsx**  
- **Elements:**  
  - User avatar  
  - User name (static)  
  - **Suggestion:** Add a dropdown menu for logout/profile editing  

---

## **Data Visualization**  

### **Chart Components:**  

- **RenderBarChartComponent**: Bar chart for body fat percentage / **Recharts**  
- **RenderLineChart**: Temporal line chart / **Recharts**  
- **RenderMetricsTable**: Health metrics table / **Grommet**  

---

## **Project Structure:**  
```
📁 viva-bem-mais/
└── 📁 frontend/
    └── 📁 src/
        ├── 📄 index.js
        ├── 📄 App.jsx
        ├── 📄 reportWebVitals.js
        ├── 📁 components/
        │   ├── 📁 cards/
        │   │   ├── 📄 RenderBarChart.jsx
        │   │   ├── 📄 RenderInsights.jsx
        │   │   ├── 📄 RenderLineChart.jsx
        │   │   ├── 📄 RenderMetricCard.jsx
        │   │   └── 📄 RenderMetricsTable.jsx
        │   └── 📁 layout/
        │       ├── 📄 Dashboard.jsx
        │       ├── 📄 Dashboard2.jsx
        │       ├── 📄 HeaderComponent.jsx
        │       └── 📄 SidebarComponent.jsx
        ├── 📁 data/
        │   └── 📄 DashboardData.jsx
        ├── 📁 pages/
        │   ├── 📁 Dashboard/
        │   │   ├── 📄 Historic.jsx
        │   │   ├── 📄 Measure.jsx
        │   │   ├── 📄 PageDashboard.jsx
        │   │   └── 📄 UploadData.jsx
        │   ├── 📁 createAccount/
        │   │   └── 📄 CreateAccount.jsx
        │   └── 📁 PageLogin/
        │       └── 📄 PageLogin.jsx
        └── 📁 router/
            └── 📄 AppRouter.jsx
```

---

Agora a documentação inclui as instruções para rodar o projeto. Me avise se precisar de mais algo! 🚀
