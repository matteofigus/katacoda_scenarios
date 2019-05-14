# Writing new templates

CloudFormation templates are very easy to read but writing a new template requires memorising the properties of each resource you are creating.

AWS Cloudformation Template Builder is a command line tool and Go library that consumes the published [CloudFormation specification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-resource-specification.html) and generates skeleton CloudFormation templates with mandatory and optional parameters of chosen resource types pre-filled with placeholder values.

## Step 1: Install 

AWS CloudFormation Template Builder can be installed using snap:
`snap install cfn-skeleton`{{execute}}

*Mac user? You can install as Go binary too!*

## Step 2: Try it

Now you can see the available commands by typing:

`cfn-skeleton`{{execute}}

## Step 3: Create a new template

Let's create a simple template for a Bucket and an Instance.

`cfn-skeleton Bucket EC2::Instance`{{execute}}

Well, that's a lot of stuff! You can use the `-b` parameter for creating the bare minimum configuration:

`cfn-skeleton -b Bucket EC2::Instance`{{execute}}

## Conclusion

We'll remind you the repo link at the end of the tutorial: [github.com/awslabs/aws-cloudformation-template-builder](https://github.com/awslabs/aws-cloudformation-template-builder).

Now go to the next step to learn about another tool.
