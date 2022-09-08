pipeline
{
  agent any
  
  //environment
  //{
    //registry="public.ecr.aws/g9t7d5z8/dockerdemo"
  //}
  
  stages
  {
    //stage("Docker Build")
    //{
      //steps
      //{
        //script
        //{
          //dockerImage=docker.build registry
        //}
      //}
    //}
    //stage("Docker Push")
   // {
      //steps
      //{
       // script
       // {
        //  bat 'aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/g9t7d5z8'
        //  bat 'docker build -t dockerdemo .'
        //  bat 'docker tag dockerdemo:latest public.ecr.aws/g9t7d5z8/dockerdemo:latest'
        //  bat 'docker push public.ecr.aws/g9t7d5z8/dockerdemo:latest'
       // }
     // }
   // }
    stage("Test")
    {
      steps
      {
        bat 'python3 hello.py'
      }
    }
    
  }
}
