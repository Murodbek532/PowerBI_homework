## Lesson 19

**Topic: Publishing and Sharing in Power BI**

---

### 1. Difference between Power BI Desktop and Power BI Online Service

**Power BI Desktop** is a local application used to:

* connect to data sources,
* transform and model data,
* create relationships and DAX measures,
* design reports.

**Power BI Online Service** is a cloud-based platform used to:

* publish reports,
* share content with others,
* manage access and security,
* schedule data refreshes,
* create dashboards and apps.

Desktop is for **development**, while the Service is for **distribution and collaboration**.

---

### 2. How to publish a report from Desktop to Online Service

1. Open the report in Power BI Desktop
2. Select **Home → Publish**
3. Sign in to your Power BI account
4. Choose a target **workspace**
5. After publishing, the report and semantic model appear in Power BI Service

---

### 3. What is a workspace in Power BI? Types of workspaces

A **workspace** is a container in Power BI Service that stores:

* reports,
* datasets (semantic models),
* dashboards,
* dataflows.

**Types of workspaces**:

* **My Workspace** – personal, not intended for collaboration
* **Shared (App) Workspaces** – used for team collaboration and app publishing

---

### 4. Difference between a workspace and an app

* A **workspace** is where content is created and managed.
* An **app** is a packaged and read-only version of that content for end users.

Workspace = development and management
App = controlled consumption

---

### 5. Power BI license types and their limitations

**Free**

* View content only in My Workspace
* No sharing or collaboration

**Pro**

* Publish and share reports
* Collaborate in workspaces
* Scheduled refresh

**Premium Per User (PPU)**

* Advanced features and larger models
* Requires PPU for both creators and viewers

**Premium Capacity**

* Dedicated cloud resources
* Free users can view shared content
* Designed for enterprise environments

---

### 6. Sharing a report with someone without a Pro license

This is possible only when:

* the report is stored in a **Premium capacity workspace**, or
* the report is published as an **App** in Premium capacity, or
* Power BI Embedded is used.

Without Premium, Free users cannot view shared reports.

---

### 7. What is a semantic model (dataset) and where it is stored

A **semantic model (dataset)** contains:

* tables,
* relationships,
* measures,
* security rules (RLS).

It is stored in **Power BI Service inside the workspace** after publishing.

---

### 8. How Scheduled Refresh works in Power BI Service

Scheduled Refresh:

* is configured in **dataset settings**,
* requires data source credentials,
* requires a gateway for on-premises data,
* refreshes data automatically on a schedule.

---

### 9. Difference between a dataset and a dataflow

**Dataset (semantic model)**:

* supports reports and visuals,
* includes relationships and DAX.

**Dataflow**:

* performs data preparation in the cloud,
* uses Power Query Online,
* can be reused by multiple datasets.

---

### 10. When and why to use a dataflow instead of a dataset

Dataflows are used when:

* multiple reports require the same prepared data,
* centralized data transformation is required,
* consistent business logic is needed.

They act as a **shared data preparation layer**.

---

### 11. What are dashboards and how they differ from reports

**Dashboards**:

* exist only in Power BI Service,
* consist of pinned tiles,
* have a single-page layout,
* are not fully interactive.

**Reports**:

* can have multiple pages,
* support filtering and drilling,
* are created in Power BI Desktop.

---

### 12. How to pin a visual to a dashboard

1. Open the report in Power BI Service
2. Hover over a visual
3. Select **Pin visual**
4. Choose an existing or new dashboard

---

### 13. What is the mobile view and why it is useful

The **mobile view**:

* optimizes report layout for mobile devices,
* improves readability and usability,
* provides a better experience for users on phones.

---

### 14. What is a paginated report and when to use it

A **paginated report**:

* is designed for printing,
* uses a fixed page layout,
* supports large tabular data.

It is used for invoices, financial statements, and operational reports.

---

### 15. Exporting reports to PDF or PowerPoint

Reports can be exported:

* in Power BI Service,
* via **File → Export → PDF / PowerPoint**,
* availability depends on license and permissions.

---

### 16. What “Live Connection” means in Power BI

A **Live Connection**:

* connects directly to a dataset or Analysis Services model,
* does not import data into the report,
* always shows current data,
* does not allow model editing.

---

### 17. Row-Level Security (RLS) in Power BI

**Row-Level Security (RLS)** restricts data visibility by user:

* defined in Power BI Desktop,
* published to the Service,
* users are assigned to roles in the Service.

---

### 18. How to test RLS roles in Power BI Service

* In Desktop: **Modeling → View as**
* In Service: **Dataset → Security → Test as role**

---

### 19. What are Apps in Power BI and how to publish them

**Apps** are curated packages of content for end users.

**Publishing steps**:

1. Open a workspace
2. Select **Create app**
3. Configure navigation and permissions
4. Publish the app

---

### 20. Key benefits of Power BI Online Service in enterprise environments

* Centralized content management
* Secure data access and RLS
* Scheduled refresh
* App distribution
* Scalability
* Collaboration and governance
