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
   
    stage('Checkout'){
      steps{
      	git credentialsId: '7e688974-2bea-4d9a-98d2-adc25016f90d', poll: false, url: 'https://github.com/alexndi/hwrepo'
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


