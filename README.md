# My Collection of CFN Templates

The following are CloudFormation templates that standup common resources and to be used as a starting point for creating other resources. Below are descriptions of the generic templates I've created. Each section will have a block of required parameters and a list of exported values.

## VPC
The VPC template creates a VPC with a public subnet and a private subnet. The public subnet has an Internet Gateway and the private subnet has a NAT Gateway. Both have route tables out to the public internet through their respective gateways.

### Parameters
* VPCCidr
    - IPv4 range (in CIDR) for the VPC. It should be in the form `xxx.xxx.xxx.xxx/16-24`. The default value is 10.0.0.1/16.
* PublicCidr
    - IPv4 range (in CIDR) for the public subnet. It should be in the form `xxx.xxx.xxx.xxx/16-24`. The default value is 10.0.1.1/24.
* PrivateCidr
    - IPv4 range (in CIDR) for the private subnet. It should be in the form `xxx.xxx.xxx.xxx/16-24`. The default value is 10.0.2.1/24.

### Exports
* VPCID
    - The ID of the VPC.
* PubSubnetID
    - The ID of the private subnet.
* PrivSubnetID
    - The ID of the private subnet.
* NATGWIP
    - The IP address of the elastic IP attached to the NAT Gateway.
* NATGatwayID
    - The resource name of the NAT Gateway attached to the private subnet.
* InternetGatwayID
    - The resource name of the Internet Gateway attached to the public subnet.


## Config
The Config template creates a configuration recorder for all resources in a region and all non-region based resources as well. A single rule is provided to show how it's used.

### Parameters
* AWSRegion

### Exports
*
