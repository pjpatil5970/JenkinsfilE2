pipeline {
  agent anY

  stages {
    parameters {
       string defaultValue: 'TEST', description: 'ENVIRONMENT FOR DEPLOY', name: 'ENV', trim: true
       choice choices: ['main', 'master'], description: 'envirnoment for deployment of app', name: 'BRANCH'
    } 
    environment {
	    DEPLOY_BRANCH = "$BRANCH"
	    DEPLOY_ENV = "$ENV"
    }

    stage ('BUILD') {
      steps {
        echo "Deploying to $(param.ENV)" 
	echo "code from $(param.BRANCH) branch"
        sh ''' 
		sleep 5
	        exit 0 
	   '''
      }  
    }  
    
    stage ('TEST') {
      steps {
        echo "This is Test stage" 
        sh 'sleep 5; exit 0'
      }  
    }  
    
    stage ('DEPLOY') {
      steps {
        echo "This is Deploy stage" 
        sh 'sleep 5'
      }  
    }  
  } 

}
