pipeline{
	agent any
	stages {
	  stage('build'){
      git 'https://github.com/PrachiJukaria/django-todo-cicd.git'
    }	
    stage('deploy')
    {
      script{
        sh 'docker build -t todo-cicd .'
        sh 'docker run -d -p 8000:8000 todocicd'
      }
    }
  
	}
}
