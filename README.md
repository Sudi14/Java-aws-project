*Creating CodePipeline using CloudFormation*

aws cloudformation create-stack --stack-name demo_build_project --template-body file://cfn/pipeline.yml --parameters file://cfn/pipeline-parameter.json --capabilities CAPABILITY_NAMED_IAM


*With HTTPS connections and Git credentials, you generate a static user name and password in IAM.*

git clone https://git-codecommit.us-east-2.amazonaws.com/v1/repos/MyDemoRepo my-demo-repo

Create Project files and buildspec.yml in my-demo-repo folder

git add .
git commit -m "initial Commit"
git push origin master ** May Ask about generated credential(https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up.html, https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-connect.html)