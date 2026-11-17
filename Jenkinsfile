pipeline
{
  agent any
  
  environment
  {
    PATH="/opt/maven/bin:$PATH"
  }
  
  stages
  {

    stage('Build Code')
    {
      steps
      {
        sh 'mvn clean deploy -Dmaven.test.skip=true'
      }
    }

    stage('Test Code')
    {

      steps
      {

        sh 'mvn clean test surefire-report:report'
      }

    }
 }
 
}   
    


