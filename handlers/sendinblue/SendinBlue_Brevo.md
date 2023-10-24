# Welcome to the MindsDB Manual QA Testing for SendinBlue(Brevo) Handler


## Testing SendinBlue Handler

**1. Testing CREATE DATABASE**

```sql

CREATE DATABASE sib_datasource
WITH ENGINE = 'sendinblue',
PARAMETERS = {
  "api_key": "xkeysib..."
};

```

![CREATE DATABASE](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/4aedf6e9-a679-4f44-a64c-73523880b21b)


**2. Testing CREATE Promotional Email**

![image](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/b55ef968-9b64-425d-afdd-30bad86358a8)

**3. Testing SELECT FROM email_campaigns**

```sql

SELECT * FROM sib_datasource.email_campaigns;
```

![SELECT FROM](https://github.com/adeyinkaezra123/mindsdb-integration-test/assets/65364356/e990ebb7-3bb4-4d68-9a48-7cc32b5f9b70)





### Results

Drop a remark based on your observation.
- [x] Works Great 💚 (This means that all the steps were executed successfully and the expected outputs were returned.)
- However, a small *non-intrusive* exception is being raised upon querying the Sendinblue datasource for email campaigns

---


