pipeline {
  agent any
parameters {
       string defaultValue: 'TEST', description: 'ENVIRONMENT FOR DEPLOY', name: 'ENV', trim: true
       choice choices: ['main', 'master'], description: 'envirnoment for deployment of app', name: 'BRANCH'
    } 
 environment {
	    DEPLOY_BRANCH = "$BRANCH"
	    DEPLOY_ENV = "$ENV"
 }
stages {
    stage ('BUILD') { 
      steps {
        echo "Deploying to ${params.ENV}" 
	echo "code from ${params.BRANCH} branch"
        sh ''' 
		sleep 5
                echo Deploying to $(DEPLOY_ENV) 
	         echo code from $(DEPLOY_BRANCH) branch
          
              
	        exit 0 
	   '''
      }  
    } 

}
}
