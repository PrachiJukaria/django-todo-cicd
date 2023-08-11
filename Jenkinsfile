pipeline{
	agent any
	stages {
	  // 	stage('build'){
   //    			steps{
			// 	checkout scmGit(branches: [[name: '*/develop']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/PrachiJukaria/django-todo-cicd']])
			// }
   //  		}	
    		stage('deploy')
    		{
      			steps{
				script{
        				sh 'docker build -t todo-cicd:2 .'
        				sh 'docker run -d -p 8000:8000 todo-cicd:2'
      				}
			}
    		}
  
	}
}
