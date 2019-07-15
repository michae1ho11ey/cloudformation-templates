# My Collection of CFN Templates

The following are CloudFormation templates that standup common resources and to be used as a starting point for creating other resources. Below are descriptions of the generic templates I've created. Each section will have a block of required parameters and a list of exported values.

## VPC
The VPC template creates a VPC with a public subnet and a private subnet. The public subnet has an Internet Gateway and the private subnet has a NAT Gateway.

### Parameters
* 

### Exports
* 


## Config
The Config template creates a configuration recorder for all resources in a region and all non-region based resources as well. A single rule is provided to show how it's used.

### Parameters
* AWSRegion

### Exports
* 
