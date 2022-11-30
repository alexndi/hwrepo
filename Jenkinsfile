pipeline{

  agent {
      label 'windows'
  }
  
  parameters{
      string(name:'Version', defaultValue:'abc', description:'initial version')      
  }
  
  stages{
    stage('Build'){
      steps{
      	echo "Hello from build"
      }
    }
    
    stage('Test'){
      when{
        expression{
            env.NODE_NAME == "Local Node"
        }
      } 
    
      steps {
      	echo "Hello from test"
      }
    }
    stage('Publish') {
      steps {
      	echo "Hello from publish"
      }
    }
  }
    
 post {
      always {
          echo "shutdown machine"
      }
      
      success {
          echo "congratulations!"
      }
      
      failure {
          echo "send mail for failure"
      }
    }
  }  


