Install CLI
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
check instaltion
aws --version
configure credentians and insert your access key id
aws configure
execute this command to create vpc
aws cloudformation deploy --region=us-east-1 --stack-name=laravel-vpc --template-file ./.aws/vpc.yaml
execute this command to create the instances
aws cloudformation deploy --region=us-east-1 --stack-name=laravel-web --template-file ./.aws/infrastructure.yaml --capabilities CAPABILITY_IAM --capabilities CAPABILITY_NAMED_IAM 
