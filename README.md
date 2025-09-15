# n8n E-commerce Order Processing Automation

This repository contains my **Assessment Task for n8n**:  
**Task 1 – E-commerce Order Processing Automation**.

---

## 📌 Workflow Features

- **Order Intake**
  - Webhook node receives new orders from the e-commerce platform.
- **Validation**
  - Ensures required fields (`order_id`, `email`, `items`, `status`) are present.
- **Payment Verification**
  - Verifies payments using Stripe Test API before processing.
- **Inventory Management**
  - Reads product stock levels from Google Sheets.
  - Checks if ordered items are in stock.
  - Updates inventory automatically after successful orders.
  - Sends low-stock alerts when stock falls below threshold.
- **Invoice Generation**
  - Creates PDF invoice with order + customer details.
  - Sends invoice via email to customer after successful order.
- **Error Handling**
  - Dedicated error workflow captures and logs failures.
  - Admin notified via email in case of workflow errors.
- **Sales Reporting**
  - Appends each order into a sales log sheet.
  - Generates daily sales analytics and charts using QuickChart.
  - Sends daily sales report by email.
  - Dashboard with 3 charts created in Google Sheets.

---

## 📂 Repository Contents

- `Ecommerce Order Processing Automation.json`  
  → Complete n8n workflow JSON file (import into n8n).  

- `README.md`  
  → Project documentation.

---

## 🚀 How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/n8n-ecommerce-automation.git
   ```
2. Open n8n (running locally or in Docker).

3. Go to Workflows → Import from File.

4. Select Ecommerce Order Processing Automation.json.

5. Update credentials for:
  - Google Sheets (Inventory & Sales log)
  - Email/SMTP (customer + admin notifications)
  - Stripe (test API key for payment verification)
    
---

## Screenshot of Workflow

