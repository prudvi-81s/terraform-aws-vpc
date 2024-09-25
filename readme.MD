# Terraform AWS VPC Module Customised

This module is going to create the following resources. for we are going to get first 2 az

* vpc
* internet gateway associated with vpc
* 2 public subnets
* 2 private subnets
* 2 database subnets
* database subnet group
* eip
* nat gateway
* public route table
* private route table
* database route table
* routes
* route table associations with subnets
* peering with default vpc(if required)
* perring routes in acceptor and requestor route tables

# inputs
* Project_name (mandatory) : user must supply theri project name
* environment (mandatory) : user must supply theri environment name
* vpc_cidr (mandatory) : user must supply theri vpc cidr.
* enable_dns_hostnames (optional): defaults true.
* common_tags (optional) : default is empty.user can supply tags in list(string) format.
* vpc_tags (optional) : default is empty.user can supply tags in list(string) format.
* igw_tags (optional) : default is empty.user can supply tags in list(string) format.
* public_subnet_cidrs (mandatory): user must supply only 2 valid public subnet CIDR
* public_subnet_tags (optional) : default is empty. user can supply tags in list(string) format.
* private_subnet_cidrs (mandatory): user must supply only 2 valid public subnet CIDR
* private_subnet_tags (optional) : default is empty. user can supply tags in list(string) format.
* database_subnet_cidrs (mandatory): user must supply only 2 valid public subnet CIDR
* database_subnet_tags (optional) : default is empty. user can supply tags in list(string) format.
* db_subnet_group_tags (optional) : default is empty.user can supply tags in list(string) format.
* nat_gateway_tags (optional) : default is empty.user can supply tags in list(string) format.
* public_route_table_tags (optional) : default is empty.user can supply tags in list(string) format.
* private_route_table_tags (optional) : default is empty.user can supply tags in list(string) format.
* database_route_table_tags (optional) : default is empty.user can supply tags in list(string) format.
* is_peering_required (optional): defaults to false
* vpc_peering_tags (optional): default is empty. user can supply tags in list(string) format.

# OUTPUTS
* vpc_id: vpc id created
* public_subnet_ids: list of 2 public subnet ids created
* private_subnet_ids: list of 2 private subnet ids created
* database_subnet_ids: list of 2 database subnet ids created
