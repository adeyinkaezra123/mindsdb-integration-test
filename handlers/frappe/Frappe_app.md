# Welcome to the MindsDB Manual QA Testing for the Frappe app integration

## Testing Frappe Handler

**1. Testing CREATE DATABASE**

```sql

CREATE DATABASE my_frappe
WITH
  ENGINE = 'frappe'
  PARAMETERS = {
    "access_token": "XXXXX....",
    "domain": "https://mindsdb.frappe.cloud"
  };

```

![image](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/0c78a95f-7d6f-46e9-a3de-35992736b54f)


**2. Testing SELECT DOCUMENTS from Doctypes**

```sql
SELECT * FROM my_frappe.documents
WHERE
  doctype = 'Expense Claim';
```
![image](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/32c10e88-8a6a-4e77-864e-d5d415899eff)



**3. Testing SELECT DOCUMENTS from Doctypes with constraint clause**

```sql

SELECT * FROM sib_datasource.email_campaigns;
```
![SELECT DOCUMENTS](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/0a026f85-5520-4222-a7f8-20dd6e6f0cf3)



**4. Testing INSERT New DOCUMENT into DOCTYPE**

```sql
INSERT INTO my_frappe.documents (doctype, data)
VALUES ('Expense Claim', '{ 
  "name": "MindsDB Expense Claim" ,
  "posting_date": "2023-05-15",
   "company": "MindsDB", 
   "amount": "100" }'
   );
```

![INSERT INTO DOCTYPES](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/99363c78-6418-4429-9197-c2d859109d0b)


**Result on the Frappe web app**

![FRAPPE UI](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/5452fce0-9f7e-47a9-b4d8-bb1a9fdd33d6)


### Results

Drop a remark based on your observation.
- [x] Works Great 💚 (This means that all the steps were executed successfully and the expected outputs were returned.)
---


