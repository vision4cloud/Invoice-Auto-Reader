# Invoice Auto Extractor 

This project automatically extracts GSTIN, Invoice Date, and Total Amount from uploaded invoice PDFs using AWS Textract's Analyze Expense API, and sends the extracted info via email using SNS.

It’s a completely serverless and scalable solution — perfect for businesses who want to automate invoice data entry and reduce manual work.

# Problem Statement

Most small and medium businesses receive 100s of invoices per month.  
Usually, accountants manually open each PDF invoice and note down:
- GSTIN
- Invoice Date
- Total Amount

This process is:
- Time-consuming 
- Prone to human error 
- Boring and repetitive 

# Solution: Serverless Invoice Extractor using AWS

Whenever a user uploads an invoice to an S3 bucket:
1. Lambda function is triggered
2. It calls Textract's Analyze Expense API to extract structured data
3. It parses GSTIN, Date, and Amount
4. Sends the data via email using SNS

- Fully automated  
- Serverless (low cost, no maintenance)  
- Real-world business use-case  

# Technologies Used

Amazon S3       > To store invoice PDFs 
Amazon Textract >  To extract data from the invoice 
AWS Lambda      > To process the Textract output 
Amazon SNS      > To send email notifications 
IAM Roles       > To grant permission to Lambda 
CloudWatch Logs > For debugging and monitoring 

# Architecture Diagram

( *To be added: `architecture.png` or Draw.io link here*)

Upload Invoice → S3 Bucket → Lambda Triggered →
→ Textract Analyze Expense →
→ Extract GSTIN, Date, Amount →
→ SNS Notification
