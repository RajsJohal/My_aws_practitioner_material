# Connectivity to AWS

## Amazon VPC
- Establish boundaries around your AWS resources.
- Enables you to provision an isolated section of the public AWS cloud.
- Within the isolated section of the cloud you can launch resources in a virtual network that you define. Within a VPC you can organize your resources into subnets. A subnet is a section of a VPC that can contain resources such as EC2 instances. 

## Internet Gateway
- To allow traffic from the internet to access your VPC, you attach an internet gateway to the VPC. 
- An internet gateway is a connection between a VPC and the internet. 

## Virtual Private Gateway
- Provides access to private resources within a VPC
- The virtual private gateway is the component that allows protected internet traffic to enter into the VPC.
- Enables you to establish a virtual private network connection between your VPC and a private network, such as on-premises data centre or internal corporate network. Only allows traffic into the VPC only if it comes from an approved network.

## AWS Direct Connect
- A service that enables you to establish a dedicated private connection between your data centre and a VPC. 
- The private connection provided by direct connect helps reduce network costs and increase the amount of bandwidth that can travel through your network. 

## Subnets
- A section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private.
- Public Subnets contain resources that need to be accessible by the public, such as an online store's website.
- Private Subnet contain resources that should accessible only through your private network, such as a database that contains customer's personal information and order histories. 
- Subnets can communicate with each other within a VPC. For example a public facing application will be located within a public subnet and retreives data from the database loated within the private subnet. 

## Network Access Control List (ACLs)
- A virtual firewall that controls inbound and outbound traffic at the subnet level. 
- Explicit rules can be defined to allow or block certain traffic coming from a specified type of connection or specific IP ranges. Otherwise the default ACL will be used which allows all inbound and outbound traffic. 

#### Stateless Packet Filtering
- Networks ACLs perform stateless packet filtering. They remember nothing and check packets that cross the subnet both inbound and outbound. 
- Network ACLs check packets against its own list of rules to determine whether to alloy or deny.
- After a packet has entered a subnet, it must have its permissions evaluated for resources within the subnet such as EC2 instances. 

## Security Groups
- A virtual firewall that controls inbound and outbound traffic for an EC2 instance.
- Default = deniy all inbound and allow all outbound traffi. 
- Custom rules can be added to configure which traffic to allow or deny.
- Multiple EC2 instances can use the same security group and can also be custom for each EC2 instance.

#### Stateful Packet Filtering
- Security groups perform stateful packet filtering. They remember previous decisions made for incoming packets.
- When a packet response for that request returns to the instance, the security group remembers your previous request. The security group allows the response to proceed, regardless of inbound security group rules. 

