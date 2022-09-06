## ABOUT
- this whole repo is about me setting up a cloud environment using SAM scripts.

### How to deploy
aws --profile abe-admin cloudformation validate-template --template-body file://testApiGateway.yml

aws --profile abe-admin cloudformation create-stack --stack-name acc8vzztest --template-body file://testApiGateway.yml --capabilities CAPABILITY_AUTO_EXPAND
aws cloudformation update-stack --stack-name aliasTest --template-body file://simpleGateway.yml --capabilities CAPABILITY_AUTO_EXPAND, CAPABILITY_IAM

aws --profile rdca cloudformation delete-stack --stack-name acc8vzztest!
