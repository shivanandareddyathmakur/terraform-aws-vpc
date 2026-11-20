### terraform aws vpc

this module creates the following resources

*vpc
*IDW
*2 public subnets in us-east-1a and us-east-1b AZ
*2 private subnets in us-east-1a and us-east-1b AZ
*2 database subnets in us-east-1a and us-east-1b AZ
*public route table
*private route table
*datbase route table
*IGW added in public route
*EIP for NAT
*NAT gateway in public subnet 1a AZ
*route table-association with subnets
*VPC to deafult peering
*public route table to default vpc route
*default vpc main route table to created vpc route
*NAT gateway route to private and database route tables

###INPUTS

*vpc-cidr - (required) - user must supply cidr for vpc
*project-name - (mandatory) - user must supply project name
*environment - (mandatory) - user must supply environment
*vpc-tags - (optional) - user must supply tags
*public-subnet-cidr - (mandatory) - user must suuply public subnet cidrs
*private-subnet-cidr - (mandatory) - user must suuply private subnet cidrs
*database-subnet-cidr - (mandatory) - user must suuply database subnet cidrs
*is-peering-required - (optional) - if you need connection with different VPC's then you need to select true
    

###outputs
VPC-ID - you will see the vpc id in the outputs
public_subnet_ids - you can see the subnet ids attached to public subnets
private_subnet_ids - you can see the subnet ids attached to private subnets
database_subnet_ids - you can see the subnet ids attached to database subnets


