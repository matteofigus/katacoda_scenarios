# Converting JSON to YAML

For years, CloudFormation only supported JSON. We released YAML support and customers wanted a way to convert their existing templates.

AWS CloudFormation Template Flip is a tool that converts [AWS CloudFormation](https://aws.amazon.com/cloudformation/) templates between [JSON](http://json.org/) and [YAML](http://yaml.org) formats, making use of the YAML format's short function syntax where possible.

The term "Flip" is inspired by the well-known Unix command-line tool [flip](https://ccrma.stanford.edu/~craig/utility/flip/) which converts text files between Unix, Mac, and MS-DOS formats.

## Step 1: Install 

AWS CloudFormation Template Flip can be installed using snap:
`snap install cfn-flip`{{execute}}

## Step 2: Try it

Now you can see the available commands by typing:

`cfn-flip`{{execute}}

## Step 3: Flip it

To test the tool we'll use a JSON: `assets/example.json`{{open}}

Reading from stdin and outputting to stdout:
`cat assets/test.json | cfn-flip`{{execute}}


## Visit the docs

Visit the Github repo to learn more about the tool and the available commands: [github.com/awslabs/aws-cfn-template-flip](https://github.com/awslabs/aws-cfn-template-flip)
