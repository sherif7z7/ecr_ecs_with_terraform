-build the image in the diectory 
  docker build -t <name-tag> .
  docker run -p 3000:3000 <name-tag>
-then run terraform file of create ecr 
  terraform init
  terraform plan
  terraform apply ecr.tf 
 - run that command to apply image in to ecr
    aws ecr get-login-password --region region | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com
    docker images
    docker tag e9ae3c220b23 aws_account_id.dkr.ecr.us-west-2.amazonaws.com/my-repository:tag
    docker push aws_account_id.dkr.ecr.us-west-2.amazonaws.com/my-repository:tag
