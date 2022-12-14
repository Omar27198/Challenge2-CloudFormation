# Challenge2-CloudFormation {Networking-Infrastructure}
Project Overview<br />
You have been tasked with creating the required Infrastructure-as-code scripts for a new cloud environment in AWS. The Lead Solutions Architect for the project sends you the following diagram.<br />

![AWSWebApp](https://user-images.githubusercontent.com/23401470/181375463-f1b93a01-60e4-4d79-b72c-b8e3b3553d9d.jpeg)

<br />
ToDo<br />
Write a CloudFormation script that:<br />
1-) Creates a VPC, It will accept the IP Range -also known as CIDR block- from an input parameter <br />
2-) Creates and attaches an Internet Gateway to the VPC<br />
3-) Creates Four Subnets within the VPC with Name Tags to call them “Public” and “Private” These will also need input parameters for their ranges, just like the VPC. The Subnet called “Public” needs to have a NAT Gateway deployed in it This will require you to allocate an Elastic IP that you can then use to assign it to the NAT Gateway. The Public Subnet needs to have the MapPublicIpOnLaunch property set to true. Use this reference for help. The Private Subnet needs to have the MapPublicIpOnLaunch property set to false. Both subnets need to be /24 in size. If you need assistance with IP math, you can use a subnet calculator such as this one.
You will need 3 Routing Tables, one named Public and the other two Private Assign the Public and Private Subnets to their corresponding Routing table<br />
4-) Create a Route in the Public Route Table to send default traffic ( 0.0.0.0/0 ) to the Internet Gateway you created<br />
5-) Create a Route in the Private Route Table to send default traffic ( 0.0.0.0/0 ) to the NAT Gateway<br />
