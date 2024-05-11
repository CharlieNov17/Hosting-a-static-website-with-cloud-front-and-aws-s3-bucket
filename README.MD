### Hosting-a-Static-Website-with-CloudFront-and-AWS-S3-Bucket
- Prerequisites-

    An AWS account. If you don't have one, you can sign up for free.
    Basic familiarity with AWS services and the AWS Management Console.
    A static website you want to host. This could be a collection of HTML, CSS, JavaScript, and image files.![aws_account](/Assignment%20Screenshot/100.png)

    1. Create an S3 Bucket

    Go to the AWS Management Console and navigate to the S3 service.
    Click on "Create bucket".
    Enter a unique bucket name and choose the region where you want to host your website.
    Disable "Block all public access" and acknowledge that the bucket will be public.
    Click "Create bucket".
    ![create a bucket](/Assignment%20Screenshot/101.png)

2. Upload Website Files to S3

    Open the bucket you created.
    Click "Upload" and select the files and folders of your website.
    Once uploaded, select the files, and in the "Actions" dropdown, choose "move", select your s3 bucket name move the files to the s3 bucket root.
    ![Upload flies](/Assignment%20Screenshot/103.png)

3. Enable Static Website Hosting on S3

    In the bucket properties, navigate to "Static website hosting".
    Select "Use this bucket to host a website" and enter the index document (e.g., index.html).
    Click "Save".![Bucketpolicy](/Assignment%20Screenshot/106.png)

4. Create a CloudFront Distribution

    Go to the CloudFront service in the AWS Management Console.
    Click on "Create Distribution".
    Choose "Web" as the delivery method.
    In the "Origin Domain Name" field, select the S3 bucket you created.
    Configure other settings as needed (e.g., default cache behavior, alternate domain names).
    Click "Create Distribution".![cloudfront_distro](/Assignment%20Screenshot/107.png)

5. Testing

    Once the CloudFront distribution is deployed (which may take some time), you can access your website using the CloudFront domain name or your custom domain if configured.![Page_rendering](/Assignment%20Screenshot/110.png)