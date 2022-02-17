This repo will contain a [CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html) template that can be used to create, and demonstrate, a simple [Step Function](https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html).

Yes, inline lambdas. The purpose is to demonstrate step functions, not setup a ci/cd pipeline to deploy lambdas :)

```sh
# create the stack
aws cloudformation create-stack \
--stack-name limit-increase \
--template-body file://template.yml \
--capabilities CAPABILITY_NAMED_IAM

# update the stack
aws cloudformation update-stack \
--stack-name limit-increase \
--template-body file://template.yml \
--capabilities CAPABILITY_NAMED_IAM
```
