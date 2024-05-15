**Hosting Static Website using Amazon S3**

This project is all about hosting a simple website using Amazon S3. This made possible by creating S3 bucket to host our website. Unselecting “Block public access” in bucket settings allow our website to be publicly accessible. Bucket policy edited as:

{

`    `"Version": "2012-10-17",

`    `"Statement": [

`    	`{

`        	`"Sid": "PublicReadGetObject",

`        	`"Effect": "Allow",

`        	`"Principal": "\*",

`        	`"Action": [

`            	`"s3:GetObject"

`        	`],

`        	`"Resource": [

`                `"arn:aws:s3:::Bucket-Name/\*"

`        	`]

`    	`}

`    `]

}

This code allow GetObject to view stuffs inside our website. Now we upload a simple html website and any picture inside our S3 bucket. 

<!DOCTYPE html>

<html lang="en">

<head>

`    `<meta charset="UTF-8">

`    `<meta name="viewport" content="width=device-width, initial-scale=1.0">

`    `<title>Hello World</title>

</head>

<body>

`    `<h1>Hello World</h1>

`    `<img src="cat-image.jpg" alt="Your Image">

</body>

</html>

This code allows to view Hello World and our selected image. That’s all, this is our easiest way to host a static website on Amazon S3!


