+++
title = 'requirements'
layout = 'requirements'
emoji= '📝'
menu_level = ['week']
weight = 3
coursework= 'Module-cloud'
coursework_filter= 'Week 1'
+++

By the end of the coursework you should have the a Frontend, Backend and Database deployed and working in AWS.

We recommend using the "CYF Hotel" project from the course but you are welcome to use any project you like.

## Note: Getting Help

If you are doing this for the first time, **this will be hard**. You **must** reach out to Volunteers to help you. Your ability to ask for help is be actively assessed during this time.

You are **not** expected to be able to complete this module completely independently. You **are** expected to get help from volunteers.

## Deploy your Frontend to S3

In this section, you will deploy the the frontend to S3.

When you have done this successfully, you should be able to access the frontend using the S3 endpoint.

To do this you will need to:

1. **Create an S3 Bucket**: Create a new S3 bucket in your AWS console.
2. **Configure S3 for Static Website**: Enable static website hosting on the bucket and note the S3 endpoint.
3. **Upload Files**: Upload the frontend HTML, CSS, and JavaScript files to the bucket. There are multiple ways to upload files to S3. Follow their documentation and choose the way that is best for you: <https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html>
4. **Set Permissions**: Make sure the bucket policy is set to allow public read access to your files.
5. **Test Your Setup**: Access the frontend using the S3 endpoint to ensure everything is working.

## Deploy your Backend to EC2

Next, you will deploy the the backend to an EC2 instance.

When you have done this successfully, you should be able to access the backend using the EC2 instance's public IP address.

To do this you will need to:

1. **Launch EC2 Instance**: Start a new EC2 instance using a suitable AMI (Amazon Machine Image).
2. **SSH into EC2**: Use SSH to access your EC2 instance. Follow the guide from AWS on how to ssh from your machine <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-ssh.html>
3. **Set up Node.js**: Install Node.js and any other dependencies.
4. **Upload Code**: Transfer your backend code to the EC2 instance. Refer to the SSH guide to transfer the code to EC2 <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-ssh.html#linux-file-transfer-scp>
5. **Start Application**: Run your Node.js application on the EC2 instance.
6. **Test API**: Test your API endpoints to make sure they're working as expected.

## Deploy your Database to RDS

Finally, you will deploy the your database to RDS.

When you have done this successfully, you should be able to access the database using the RDS endpoint.

To do this you will need to:

1. **Create RDS Instance**: In the AWS Management Console, set up a new RDS instance.
1. **Configure Security Groups**: Update security groups to allow incoming traffic on the database port you intend to use.
1. **Database Credentials**: Make a note of your database credentials (username, password).
1. **Initialize Database**: Connect to the database and initialize it with the required tables and sample data.
1. **Connect to Backend**: Update your backend code (running on EC2) to connect to the RDS database.
1. **Test End-to-End**: Make some test API calls to ensure that the data flows correctly from the RDS database to your EC2 backend, and then to the S3-hosted frontend.

## Connect all Resources

Now that you have all three elements of your project deployed, it's time to connect them together.

1. **Update** your frontend code to make API calls to your backend
2. **Update** your backend code to connect to the database.
3. **Test** your application to ensure that everything is working as expected.

When this is all working; your full stack application should now be accessible over the interview; via AWS.
