pipeline
{
  agent any
  
  environment
  {
    registry="public.ecr.aws/g9t7d5z8/dockerdemo"
  }
  
  stages
  {
    stage("Docker Build")
    {
      steps
      {
        script
        {
          dockerImage=docker.build registry
        }
      }
    }
    
  }
}
