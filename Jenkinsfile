pipeline {
  agent anY
parameters {
       string defaultValue: 'TEST', description: 'ENVIRONMENT FOR DEPLOY', name: 'ENV', trim: true
       choice choices: ['main', 'master'], description: 'envirnoment for deployment of app', name: 'BRANCH'
    } 
stages {

    stage ('BUILD') { 
	    environment {
	    DEPLOY_BRANCH = "$BRANCH"
	    DEPLOY_ENV = "$ENV"
            }
      steps {
        echo "Deploying to $(param.ENV)" 
	echo "code from $(param.BRANCH) branch"
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
