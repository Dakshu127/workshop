pipeline
{
  agent any
  
  environment
  {
    M2="/opt/maven/bin"

    PATH=$PATH:$M2
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
    


