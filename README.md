# DEMO - AWS S3 Static Website Hosting

## Overview
In this demo, I will create and configure a static website hosted on AWS S3. The process includes creating an S3 bucket, enabling static website hosting, uploading website files, and setting appropriate permissions for public access. This demo was completed using the GENERAL account, which was set up as the management account in a previous AWS Organizations demo.

## Pre-Requisites

- **AWS Account Setup**: I used the GENERAL account (management account) from my AWS Organizations setup to complete this demo.
- **Required Files**: `index.html` and `error.html` for the main website and error page.

## Steps

### 1. Create an S3 Bucket
- I navigated to the S3 service in the GENERAL account via the AWS Management Console.
- Clicked **Create Bucket**.
- Entered a globally unique bucket name `top10.animals4life.farah`.
- Unchecked **Block All Public Access** and confirmed the acknowledgment.
- Clicked **Create Bucket**.

![Screenshot](https://imgur.com/sjx3SZS.png)

### 2. Enable Static Website Hosting
- I opened the newly created bucket.
- Went to the **Properties** tab and scrolled down to the **Static Website Hosting** section.
- Clicked **Edit**, enabled the feature, and selected **Static** as the hosting type.
- Set the **Index Document** to `index.html` and the **Error Document** to `error.html`.
- Saved the changes and copied the provided static website URL.

![Screenshot](https://imgur.com/5ehpWNA.png)

### 3. Upload Website Files
- I went to the **Objects** tab in my bucket.
- Clicked **Upload** and selected the `index.html`, `error.html`, and an `img` folder needed for the static website.
- Completed the upload process.

![Screenshot](https://imgur.com/JqEieLT.png)

### 4. Access the Website (Expect 403 Error)
- I pasted the static website URL into my browser and received a **403 Forbidden** error, as the S3 bucket was private by default.

![Screenshot](https://imgur.com/DtpAoyP.png)

### 5. Update Bucket Policy for Public Access
- I navigated to the **Permissions** tab of the S3 bucket.
- Under **Bucket Policy**, I clicked **Edit**.
- I added a bucket policy granting public access.
- Saved the changes.

![Screenshot](https://imgur.com/m3EhqHN.png)

### 6. Verify Public Access
- I revisited the static website URL, and now the website was publicly accessible.

![Screenshot](https://imgur.com/roUCOGJ.png)

### 7. Clean Up
- To avoid unnecessary charges, I emptied and deleted the S3 bucket once I was done.

## Conclusion
In this demo, I used the Management account (from the AWS Organizations setup) to create a static website using S3, configured public access through bucket policies, and verified the website's accessibility. This setup allows for fast and scalable static website hosting on AWS.
