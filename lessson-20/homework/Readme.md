**1. How does Power BI handle large datasets in the Online Service, and what is the role of Premium Capacity in this?**
Power BI Service can handle large datasets either by storing them in **Import mode** or connecting via **DirectQuery/Live Connection**. For large datasets, memory and refresh limitations exist in shared capacity. **Premium Capacity** provides dedicated resources, enabling larger dataset storage (up to 400 GB per dataset in Premium Gen2), faster refreshes, higher concurrency, and advanced features like paginated reports, incremental refresh, and XMLA endpoint access for enterprise workloads.

---

**2. What are the differences between Import mode, DirectQuery, and Live Connection in Power BI Service?**

* **Import Mode**: Data is loaded into Power BI’s in-memory engine (VertiPaq). Fast performance, supports all Power BI features, but dataset size is limited by capacity.
* **DirectQuery**: Data remains in the source. Queries are executed live whenever the report is viewed. Allows real-time data access, but performance depends on the source, and some modeling features are limited.
* **Live Connection**: Similar to DirectQuery but specifically for connecting to **Analysis Services models** (SSAS or Azure AS). No data is imported; all calculations rely on the external model. Modeling options in Power BI Desktop are restricted.

---

**3. Explain deployment pipelines in Power BI Online. What stages do they include?**
Deployment pipelines provide a structured **CI/CD (Continuous Integration/Deployment)** approach for Power BI content. They include three stages:

* **Development**: Authors create and test reports/datasets.
* **Test**: Content is deployed to a testing workspace for validation.
* **Production**: Approved content is published for end-users.
  Deployment pipelines simplify version control, reduce errors, and maintain consistency across environments.

---

**4. How can Power BI Service integrate with Microsoft Teams or SharePoint for collaboration?**

* **Microsoft Teams**: Reports or dashboards can be embedded directly into Teams channels as tabs, allowing team members to interact with reports without leaving Teams. Users can receive notifications, comment, and collaborate on insights.
* **SharePoint Online**: Reports can be embedded in SharePoint pages using the Power BI web part, providing interactive reports inside intranet sites. Permissions respect Power BI dataset security.

---

**5. What is the XMLA endpoint in Premium and how does it benefit developers or enterprise BI teams?**
The **XMLA endpoint** exposes Power BI datasets as **Analysis Services objects**. Benefits include:

* Programmatic access for metadata management, automation, and advanced development.
* Support for **third-party tools** like SQL Server Management Studio (SSMS) or Tabular Editor.
* Enables complex tasks like incremental refresh, scripting, and dataset lineage management.
* Critical for enterprise teams requiring automated dataset deployment or external development workflows.

---

**6. Describe how usage metrics and audit logs work in Power BI Service.**

* **Usage Metrics**: Built-in reports that show how dashboards and reports are being consumed (views, unique users, frequency, etc.). Helps identify popular content and user engagement.
* **Audit Logs**: Captured in Microsoft 365 Compliance Center, they track user activities (e.g., data exports, sharing, sign-ins, report edits). Essential for compliance, security monitoring, and troubleshooting.

---

**7. How do you manage workspace access and permissions for different users?**
Workspaces have **roles**:

* **Admin**: Full control, including workspace settings and user management.
* **Member**: Can edit and publish content.
* **Contributor**: Can publish and update content but cannot manage access.
* **Viewer**: Can view content only.
  Access can also be restricted by **Azure Active Directory (AAD) groups**, ensuring scalable permission management.

---

**8. How can data governance be enforced in Power BI Service?**
Governance can be enforced through:

* **Row-Level Security (RLS)** to restrict data access per user.
* **Data classification and sensitivity labels** for compliance.
* **Workspace access policies** and role-based permissions.
* **Dataset certification** to indicate trusted data sources.
* **Audit logs and monitoring** to track sharing, access, and modifications.

---

**9. What are the limitations of Row-Level Security when using DirectQuery or Live Connection?**

* **DirectQuery**: RLS can be implemented in the dataset, but performance depends on source queries. Some DAX functions are unsupported.
* **Live Connection**: RLS must be defined in the underlying Analysis Services model; Power BI cannot modify it. Dynamic RLS in Power BI is not available.
* Both modes may face constraints in complex filtering and cross-source scenarios.

---

**10. Explain how you can refresh a dataset via Power Automate or REST API.**

* **Power Automate**: Use the **“Refresh a dataset”** action in flows. Triggers can include schedules, events in other systems, or approvals.
* **REST API**: Use the endpoint `POST /datasets/{datasetId}/refreshes` to trigger a refresh programmatically. Useful for integrating dataset refreshes with external processes or CI/CD pipelines.
