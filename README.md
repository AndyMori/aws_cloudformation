## ABOUT
- this whole repo is about me setting up a cloud environment using SAM scripts.

### How to deploy
aws --profile abe-admin cloudformation validate-template --template-body file://amzlin2_nginx_ec2.yml

aws --profile abe-admin cloudformation create-stack --stack-name acc8vzztest --template-body file://amzlin2_nginx_ec2.yml --capabilities CAPABILITY_NAMED_IAM
aws --profile abe-admin cloudformation update-stack --stack-name acc8vzztest --template-body file://amzlin2_nginx_ec2.yml --capabilities CAPABILITY_NAMED_IAM

aws --profile rdca cloudformation delete-stack --stack-name acc8vzztest!
