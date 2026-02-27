# 🏭 Automated Procurement & Supplier Quality ETL Pipeline

**Role:** Lead Automation Engineer  
**Tech Stack:** n8n, JavaScript, Google Workspace API, RESTful APIs  
**Domain:** Logistics & Supply Chain Management (LSCM), Supplier Relationship Management (SRM)  

## 📉 The Business Problem
Manual procurement processes often lead to two major supply chain failures: 
1. **Stockouts:** Purchasing managers fail to calculate lead times accurately, causing production halts.
2. **Poor Quality Control:** Automated systems blindly reorder from vendors with high defect rates or severe transit delays, compounding financial losses (e.g., over $8,800 in monthly defect losses).

## 🚀 The Engineering Solution
I designed and deployed a closed-loop ETL digital pipeline using **n8n** to automate inventory replenishment while enforcing strict Supplier Quality thresholds. 

The system operates on two advanced logistical algorithms written in custom JavaScript:
* **Dynamic Reorder Point (ROP):** Dynamically calculates required stock based on specific vendor Lead Times and Daily Demand: `(Daily Demand × Lead Time) + Safety Stock`. 
* **Automated Supplier Quarantine:** Cross-references real-time inventory needs against historical Vendor SLA performance. 

## ⚙️ Workflow Architecture
* **Data Extraction:** Continuously polls live inventory databases and supplier rating matrices.
* **The "Good Vendor" Route:** If a vendor maintains an SLA rating of 4.0/5.0 or higher, the system calculates the Replenishment Cycle Quantity and auto-drafts a Purchase Order.
* **The "Quarantine" Route:** If a vendor falls below the 4.0 quality threshold due to delays or defective parts, the system halts the automated PO and routes a high-priority "Emergency Sourcing" alert to the Logistics Manager.

## 📊 Project Output
*(Add your screenshots here by dragging and dropping them into this text box!)*

---
**File Included:** `SCM_Automated_Procurement_Pipeline.json` (Can be directly imported into any n8n instance).
