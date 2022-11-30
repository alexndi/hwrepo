pipeline{

agent any
  
  stages{
    stage('Build'){
      steps{
      	echo "Hello from build"
      }
    }
    
    stage('Test'){
      steps{
      	echo "Hello from test"
      }
    stage('Publish'){
      steps{
      	echo "Hello from publish"
      }
    }
  }
    post{
      always{
        echo "shutdown machine"
      }
      success{
        echo "congratulations!"
      }
      failure{
        echo "send mail for failure"
      }
    }
}
