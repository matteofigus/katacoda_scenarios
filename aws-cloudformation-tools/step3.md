# Consistent formatting of templates

The AWS documentation shows examples of templates that are formatted in a fairly consitent way with parts of the template in a particular order and resources ordered logically. In reality, when writing a new CloudFormation template (whether by hand or programatically), it can be difficult to ensure you keep to a consistent layout.

AWS Cloudformation Template Formatter is a command line tool and Go library that reads in an existing AWS CloudFormation template and outputs a cleanly-formatted, easy-to-read copy of the same template adhering to standards as used in AWS documentation. cfn-format can output either YAML or JSON as desired.

## Step 1: Install 

AWS CloudFormation Template Formatter can be installed using snap:
`snap install cfn-format`{{execute}}

## Step 2: Try it

Now you can see the available commands by typing:

`cfn-format`{{execute}}

## Step 3: Prettify a template

Try using cfn-format to prettify a template. You can use JSON or YAML as input.

`cfn-format example.json`{{execute}}

Note the way properties are sorted and prettified. This makes Diffing changes very easy!

## Conclusion

We'll remind you the repo link at the end of the tutorial, for you to take a photo in case you want to remember the link: [github.com/awslabs/aws-cloudformation-template-formatter](https://github.com/awslabs/aws-cloudformation-template-formatter).
