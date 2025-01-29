**Cloud Based e-book Delivery Solution**

The Requirements:

1.  Cloud solution that captures Email and Username from the customer.

2.  Host a website with a subscription form that asks visitors to sign
    up. In return, provide a gut-friendly recipe book. The email will be
    used for future marketing campaigns.
Cloud Based e-book Delivery Solution
3.  Ensure the e-book is only available to genuine signups.

4.  Solution without any manual administration and management on
    servers.

![](./media/image71.png)

Frontend Website & Recipe Book Storage: **Static website and Book
Repository**

Compute services & Business Logic: **Lambda Function**

Database: **Dynamo DB**

**Steps**

1.  Create amazon S3 Bucket for recipe Book

    a.  Add book/book.pdf into s3 bucket.

2.  Create Dynamo DB table

3.  Configure SES

    a.  Create identity with email address

> ![](./media/image6.png)

4.  Define IAM Policy and IAM Role for AWS Lambda

    a.  Create Policy

    b.  Create a Role for Lambda service. Attach the role to the policy
        created.

5.  Create Lambda Function and Integrate the Role

    a.  Paste the code. Set the environment variables

> ![](./media/image3.png)

6.  Build HTTP API with API Gateway (when user clicked submit button)

    a.  We build http api. Take note of the invoke url

> ![](./media/image2.png)
>
> ![](./media/image1.png)

7.  Create Amazon S3 Static Website Hosting

    a.  Upload the main files into the bucket

    b.  Even though we set it publicly accessible, we need to provide
        correct permissions.

> ![](./media/image4.png)
>
> We used a policy generator in this case.

c.  Set this website as a static website hosting service.

<!-- -->

8.  Test Application

> ![](./media/image5.png)
