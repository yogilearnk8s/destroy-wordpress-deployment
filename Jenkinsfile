pipeline {
  
  agent any  
	  options {
      timeout(time: 1, unit: 'HOURS') 
  }
  
  stages {
    stage('checkout') {
      steps {
        checkout scm
  	    }
    	}
    
     stage('terraform plan destroy') {
      steps {
	      sh 'terraform init'
	    sh 'terraform plan -destroy'
      

      }
    }

    stage('terraform destroy') {
      steps {
	    sh 'terraform destroy --auto-approve'

     }
    }

  }
  
  
}