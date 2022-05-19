# Global Networking
## Domain Name System (DNS)
- Suppose that AnyCompany has we website hosted in the AWS cloud. Customers enter the web address into their browser, and they are able to access thier website. 
- DNS Resolution involves a customer DNS resolver communicating with a company DNS server.
- DNS essentially translates domain name to an IP address. 

## Amazon Route 53
- DNS Web Service
- Provides developers and bussinses with a reliable way to route end users to internet applications hosted in AWS. 
- Amazon Route 53 connects user requests to infrastructure running in AWS. It can route users to infrastructure outside of AWS. 
- Another feature of Route 53 is the ability to manage the DNS records for domain names. 
    - You can register new domain names directly in Route 53. You can also transfer DNS records for existing domain names managed by other domain registrars. This enables you to manage all of your domain names within a single location. 

## Example: How Amazon Route 53 and Amazon CloudFront deliver content
![./images/Route53.png](Route53)

- A customer requests data from the application by going to AnyCompany's website.
- Amazon Route53 uses DNS resolution to identify AnyCompany.com's corresponding IP address. 192.0.2.0. This information is sent back to the customer.
- The customer's request is sent to the nearest edge location through Amazon CloudFront. 
- Amazon CloudFront connects to the Application Load Balancer, which sends the incoming packet to an Amazon EC2 instance. 