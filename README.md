# AWS S3 Event-Driven Automation Using Lambda

## Project Overview

This project demonstrates how I connected Amazon Simple Storage Service (Amazon S3) with AWS Lambda to automate a task when a file is uploaded to an S3 bucket. I created an S3 bucket, developed a Python Lambda function, configured an S3 trigger, uploaded a test file, and checked the execution logs in Amazon CloudWatch.

## Technologies Used

- Amazon S3
- AWS Lambda
- AWS Management Console
- Python
- Amazon CloudWatch

## Implementation Steps

### Step 1: Create an S3 Bucket

I logged in to the AWS Management Console and opened Amazon S3. I created an S3 bucket named `lambda-event-day29-10` to store the files used in the automation process.

### Step 2: Create a Lambda Function

I opened the AWS Lambda service and created a function named `S3EventDrivenAutomation`. This function contains the Python code that processes events received from Amazon S3.

### Step 3: Write the Python Code

I added Python code to the Lambda function to process the S3 event details. The code extracts information such as the bucket name and uploaded file name, prints the event details, and displays a success message.

### Step 4: Deploy the Lambda Function

After writing the code, I saved and deployed the Lambda function so that the updated code was ready to execute.

### Step 5: Configure the S3 Trigger

I added an Amazon S3 trigger to the Lambda function and selected the bucket `lambda-event-day29-10`. This connected the S3 bucket to Lambda so that the configured S3 event could automatically invoke the function.

### Step 6: Upload a Test File

I opened the S3 bucket and uploaded a file named `test.txt`. After the upload was completed, I checked the upload status and confirmed that the file was uploaded successfully.

### Step 7: Trigger the Lambda Function

When the file was uploaded, Amazon S3 generated an event that invoked the configured Lambda function. The function processed the event and retrieved details about the bucket and uploaded file.

### Step 8: Verify the Execution Using CloudWatch

I opened Amazon CloudWatch and checked the Lambda function's logs. The logs displayed the event details, uploaded file information, and success messages. This helped me verify that the Lambda function executed successfully.

## Project Result

I successfully configured event-driven automation using Amazon S3 and AWS Lambda. When I uploaded a test file to the S3 bucket, the configured trigger invoked the Lambda function, which processed the event and recorded execution details in CloudWatch Logs.

## Skills Learned

- Creating and managing Amazon S3 buckets
- Creating and deploying AWS Lambda functions
- Writing Python code to process S3 events
- Configuring S3 triggers for automatic execution
- Monitoring Lambda execution using CloudWatch Logs
- Understanding event-driven automation in AWS

## Security Note

I learned the importance of configuring AWS permissions carefully. The Lambda function should have only the permissions required to perform its tasks. Sensitive information, such as passwords and access keys, should not be stored in publicly accessible S3 buckets.

## AWS Resources Used

- **S3 Bucket:** `lambda-event-day29-10`
- **Lambda Function:** `S3EventDrivenAutomation`
- **Test File:** `test.txt`
