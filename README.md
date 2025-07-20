📊 USA Financial Data Automation Pipeline

✅ Objective:
To fully automate the process of receiving, storing, processing, and visualizing financial data—specifically credit score-related datasets—by integrating Microsoft Outlook, Power Automate, Google Drive, GCP APIs, Power BI Desktop, and Power BI Service.

End-to-End Workflow

🔹 Step 1: Automated Email Capture in Outlook
Created a dedicated Outlook folder named "Credit Data".
Applied rules to automatically filter and move emails containing credit score-related attachments to this folder, ensuring structured data capture at the source.

🔹 Step 2: Power Automate - Email to Google Drive
Leveraged Power Automate (Flow) to integrate Outlook with Google Drive.
Configured the automation to:
Trigger when a new email lands in the "Credit Data" folder.
Extract the email attachment (Excel/CSV format).
Save the attachment in a specified folder in Google Drive, creating a reliable and centralized data storage system.

🔹 Step 3: API Setup Using Google Cloud Platform (GCP)
Used Google Cloud Platform (GCP) to build a secure API that interfaces with the Google Drive folder.
Implemented authentication using OAuth 2.0 to ensure secure access.
Enabled the API to return raw file content when called from an external client (e.g., Power BI).

🔹 Step 4: Data Extraction via Python in Power BI Desktop
Within Power BI Desktop, utilized the Python scripting connector to:
Authenticate using Google’s credentials.
Call the GCP API endpoint.
Download and load the latest dataset into Power BI from Google Drive dynamically.

🔹 Step 5: Data Cleaning & Transformation in Power Query
Performed comprehensive data cleaning using Power Query (M language):
Replaced nulls/outliers with median or conditional logic.
Unified column naming conventions (e.g., replacing _ with spaces).
Handled type conversion (e.g., text to decimal) and formatting.
Appended, merged, or pivoted data as needed.

🔹 Step 6: Measure Creation (DAX Modeling)
Created dynamic DAX measures to derive key financial insights, such as:
Average Credit Score
Monthly Investment Trends
Delay Metrics from Due Dates

🔹 Step 7: Data Visualization in Power BI
Designed interactive and insightful dashboards using:
Ensured report performance optimization with proper data modeling.

🔹 Step 8: Publishing to Power BI Service
Created a dedicated Power BI Workspace titled “Financial Data”.
Published the Power BI report to this workspace for organization-wide access.
Enabled scheduled refreshes to automatically update the dataset as new data arrives via email.
