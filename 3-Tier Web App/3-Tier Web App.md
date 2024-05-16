**Building a 3-Tier Web Application on AWS**

This project aims to build a robust 3-tier web application on AWS,
leveraging multiple AWS services to ensure scalability, security, and
high availability. The architecture consists of a web tier, an
application tier, and a data tier, each hosted on separate subnets
within a Virtual Private Cloud (VPC). The setup includes configuring
network components, EC2 instances, and a LAMP server, followed by load
balancing and database setup to create a fully functional and efficient
web application infrastructure.

<img src="media/image1.png" style="width:4.59198in;height:2.08424in" />

<img src="media/image2.png" style="width:4.64592in;height:2.70849in"
alt="A screenshot of a computer Description automatically generated" />

**Network Configuration**

First, create a VPC and enable DNS hostnames and settings. Attach an
Internet Gateway to the VPC and create three sets of subnets: public
subnets for the web tier, and private subnets for both the application
and data tiers. Enable auto-assign IP addresses for the public subnets.
Next, set up route tables: a public route table with a route to the
Internet Gateway, and private route tables for the application and data
tiers with routes to a NAT Gateway, which should be created in a public
subnet with an allocated Elastic IP.

**Setting Up EC2 Instances**

Create a bastion host EC2 instance to provide secure access to instances
in private subnets. Then, create two EC2 instances for the application
tier and configure the bastion host to access these application servers.
Establish secure connections between the bastion host and the
application servers.

**Setting Up the LAMP Server**

Prepare the server by installing and configuring Apache, MariaDB, and
PHP on Amazon Linux 2. Ensure all packages are up-to-date and follow the
AWS tutorial for detailed installation steps. Test the LAMP server by
creating a PHP file and accessing it via a web browser. Secure the
database server and optionally install phpMyAdmin. Detailed instructions
can be found in the AWS LAMP Setup Tutorial.
https://docs.aws.amazon.com/linux/al2/ug/ec2-lamp-amazon-linux-2.html

**Load Balancer Configuration**

Create a load balancer to distribute traffic across the application
servers, ensuring scalability and high availability. Set up a security
group to allow traffic from the load balancer to the web servers, and
define a target group to manage the application instances.

**Database Setup**

Create a subnet group for the database instances and set up the database
in the appropriate subnets. Configure the necessary settings to ensure
proper connectivity and security.

By following these steps, you will establish a robust and scalable
3-tier web application infrastructure on AWS, ensuring effective network
connectivity, secure access, load balancing, and comprehensive database
management.

<img src="media/image3.png" style="width:4.58875in;height:1.98426in"
alt="A screenshot of a computer Description automatically generated" />
