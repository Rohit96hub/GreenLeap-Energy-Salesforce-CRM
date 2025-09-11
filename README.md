# ☀️ GreenLeap Energy Solutions CRM

A comprehensive Salesforce CRM solution designed to automate the lead-to-installation lifecycle for a modern renewable energy company. This project showcases a full-stack implementation using both declarative and programmatic Salesforce tools.

**Live Demo/Portfolio Link:** [Your Portfolio Link Here - e.g., a short screen recording]

---

### 📋 Table of Contents
1. [Problem Statement](#-problem-statement)
2. [Key Features & Solution](#-key-features--solution)
3. [Architecture & Data Model](#-architecture--data-model)
4. [Technical Highlights](#-technical-highlights)
5. [Setup & Installation](#-setup--installation)
6. [Project Phases Walkthrough](#-project-phases-walkthrough)

---

### 🎯 Problem Statement

GreenLeap Energy, a growing solar panel installation company, struggles with a disconnected and manual sales and project management process. Key challenges include:
* In-efficient lead management from multiple channels.
* Inaccurate and time-consuming manual quoting for solar installations.
* Lack of real-time visibility into project milestones for customers and internal teams.
* Poor coordination of field technician schedules for site surveys and installations.

### ✨ Key Features & Solution

This project solves these challenges by providing a unified platform to manage the entire customer journey.

| Feature                      | Implementation                                                                                                        | Business Value                                                  |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **Lead & Opportunity Mgmt** | Standard Objects, Validation Rules, Lead Conversion Mapping                                                           | 360-degree view of the customer and a streamlined sales process |
| **Automated Energy Quoting** | A guided **Screen Flow** that calculates system size, cost, and potential savings.                                      | Reduces quoting errors and accelerates the sales cycle.         |
| **Project Milestone Tracking** | Custom `Project__c` object with an **Apex Trigger** to update status and a **Platform Event** for real-time alerts.    | Enhances customer communication and internal visibility.        |
| **Energy Savings Visualizer**| A **Lightning Web Component (LWC)** with `Chart.js` on the Account page to visualize projected monthly energy savings. | Provides a clear, compelling ROI visualization for customers.   |
| **Field Technician Dispatch**| **Salesforce Maps Lite** to visualize installation sites and optimize daily routes for technicians.                       | Improves operational efficiency and reduces travel time.        |
| **Managerial Dashboards** | Custom **Reports & Dashboards** tracking lead conversion rates, sales pipeline, and project completion times.           | Enables data-driven decision-making for management.             |

---

### 🏗️ Architecture & Data Model

The solution is built on a custom data model centered around the `Account` and `Opportunity` objects, extended with custom objects to manage energy projects and system configurations.

**Entity Relationship Diagram (ERD):**

*(This is a placeholder. You will create this diagram in Phase 3 and embed the image here.)*
``

---

### 🛠️ Technical Highlights

* **Automation:** Extensive use of **Flow Builder** for complex business logic and **Apex Triggers** for data integrity and event-driven actions.
* **User Interface:** Dynamic and responsive UI built with **Lightning Web Components (LWC)** and the Lightning Design System.
* **Integration:** Mock REST API Callout from Apex to an external service for retrieving local energy rebates.
* **Event-Driven Architecture:** Utilizes **Platform Events** to decouple business processes and provide real-time notifications.
* **DevOps:** Source-driven development model using **Salesforce DX** and version control with **Git/GitHub**.

---

### 🚀 Setup & Installation

To deploy this project to a Salesforce Scratch Org:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/GreenLeap-Energy-Salesforce-CRM.git](https://github.com/YOUR_USERNAME/GreenLeap-Energy-Salesforce-CRM.git)
    cd GreenLeap-Energy-Salesforce-CRM
    ```

2.  **Authorize a Dev Hub:**
    ```bash
    sfdx auth:web:login --setalias myhuborg --setdefaultdevhubusername
    ```

3.  **Create a Scratch Org:**
    ```bash
    sfdx force:org:create --setalias GreenLeap --definitionfile config/project-scratch-def.json --durationdays 30
    ```

4.  **Push Source Code:**
    ```bash
    sfdx force:source:push
    ```

5.  **Assign Permission Sets:**
    ```bash
    sfdx force:user:permset:assign --permsetname GreenLeap_Admin
    ```

6.  **Import Sample Data:**
    ```bash
    sfdx force:data:tree:import --plan ./data/sample-data-plan.json
    ```

7.  **Open the Org:**
    ```bash
    sfdx force:org:open
    ```

---

### 🗺️ Project Phases Walkthrough

This project was built following the 10-phase project lifecycle, covering everything from initial analysis to final deployment.

*(Here, you will later add brief descriptions of what you accomplished in each phase, linking to specific parts of your code or project.)*

* **Phase 1-2:** Requirement Gathering & Org Setup
* **Phase 3:** Data Modeling (`/force-app/main/default/objects/`)
* **Phase 4:** Process Automation (`/force-app/main/default/flows/`)
* **Phase 5:** Apex Development (`/force-app/main/default/classes/` & `triggers/`)
* ... and so on.
