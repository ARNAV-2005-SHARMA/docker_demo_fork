pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        sh 'printenv'
        
      }
    }
    stage ('Publish ECR'){
      steps{
        withEnv(["AWS_ACCESS_KEY_ID=$(env.AWS_ACCESS_KEY_ID)","AWS_SECRET_ACCESS_KEY=$(env.AWS_SECRET_ACCESS_KEY)","AWS_DEFAULT_REGION=$(env.AWS_DEFAULT_REGION)"]){
          sh 'docker login -u AWS -p $(aws ecr-public get-login-password --region us-east-1) public.ecr.aws/g9t7d5z8'
          sh 'docker build -t dockerdemo .'
          sh 'docker tag dockerdemo:""$BUILD_ID""'
          sh 'docker push public.ecr.aws/g9t7d5z8/dockerdemo:""$BUILD_ID""'
        }
      }
    }
  }
}
