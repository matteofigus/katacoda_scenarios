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

To test the tool let's create a basic JSON template:
`echo '{"Description": "Test","Foo": { "Fn::Join": [" ", ["The", { "Ref": "cake" }, "is", "a", "lie"]] },"Bar": { "Fn::Base64": { "Ref": "Binary" } },"Baz": { "Fn::Sub": ["The cake is a...\n${CakeStatus}", { "CakeStatus": "lie" }] }}' >> example.json`

Reading from stdin and outputting to stdout:
`cat example.json | cfn-flip`{{execute}}

Reading from a file and outputting to stdout:

`cfn-flip examples/test.yaml`{{execute}}

Reading from a file and outputting to another file:

`cfn-flip examples/test.json output.yaml`{{execute}}

Reading from a file and cleaning up the output:

`cfn-flip -c examples/test.json`{{execute}}

## Conclusion

We'll remind you the repo link at the end of the tutorial, for you to take a photo in case you want to remember the link: [github.com/awslabs/aws-cfn-template-flip](https://github.com/awslabs/aws-cfn-template-flip).

Now go to the next step to learn about another tool.
 