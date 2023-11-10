## cross  referenced cloudformation stacks

This example demonstrates restricting cross-stack references to outputs.
**networkstack.yaml** outputs required resource to **webstack.yaml**

### networkstack.yaml 
This stack describes:

- a network stack with a VPC
- a security group
- a subnet for public web applications
- a separate public web application stack
- using the *Export* output field to flag the value of a resource output for export

### webstack.yaml
This stack describes:

- creating a cross-stack reference: it uses the Fn::ImportValue intrinsic function to import the value. 

### AWS Services involved
Amazon VPC, Amazon EC2, and AWS CloudFormation.