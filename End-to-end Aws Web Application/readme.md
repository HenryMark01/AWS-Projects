This project is about creating a web application that performs
mathematical operations. It involves hosting a webpage on Amazon
Amplify, implementing backend functionality using AWS Lambda for
calculations, utilizing API Gateway for interaction, storing data in
DynamoDB, and presenting the application through a user-friendly
interface.

<img src="Picture1.png" style="width:6.70785in;height:3.22807in"
alt="A screen shot of a computer Description automatically generated" />

1.  Firstly, our webpage finds a cozy home on Amazon Amplify, where we
    upload the "Index.html" file after zipping it up.

2.  Using AWS Lambda, we summon our Lambda function, now armed with
    updated code from "PowerOfMathFunction - Lambda-ORIGINAL," enabling
    it to perform mathematical operations. We ensure its functionality
    through a carefully configured test event.

<img src="Picture2.png" style="width:5.2951in;height:2.3977in"
alt="A screenshot of a computer Description automatically generated" />

3.  To activate our Lambda function, we need a public URL. Enter API
    Gateway! We choose a Rest API for this task.

<img src="Picture3.png" style="width:4.64959in;height:2.68228in"
alt="A screenshot of a computer Description automatically generated" />

API Gateway gets the green light to trigger our Lambda function. We also
enable CORS (Cross-Origin Resource Sharing) to allow our web
application, hosted on Amplify, to access resources across different
domains. After deploying the API, we run tests on the method body to
confirm its accuracy.

<img src="Picture4.png" style="width:2.78377in;height:1.65101in" />

4.  Let's talk data storage! DynamoDB steps in as our lightweight,
    non-relational database of choice. We grant permissions for our
    Lambda function to write to this database. After creating our
    DynamoDB table, we give our Lambda function the green light to
    access it, thanks to the "add permission" option. The necessary JSON
    code is sourced from the "Execution Role Policy JSON" file.

<img src="Picture5.png" style="width:4.5109in;height:1.44419in"
alt="A screenshot of a computer Description automatically generated" />

Enhancements await! We update our Lambda function with the code from
"PowerOfMathFunction - Lambda-FINAL," allowing us to timestamp our data
entries. A sample of our DynamoDB data demonstrates this functionality.
<img src="Picture6.png" style="width:4.49558in;height:1.47528in" />

5.  And with a simple refresh of our Amplify link, behold our Math
    Application in all its glory! Hooray!

<img src="Picture7.png" style="width:5.17227in;height:2.51815in"
alt="A screenshot of a computer Description automatically generated" />
