pipeline {
    environment {
        registry = "rsureshk/capstone-project"
        registryCredential = 'dockerhub'
        dockerImage = ''
                }
    agent any
   
   stages {

		    stage('Lint HTML') {
			      steps {
				        sh 'tidy -q -e *.html'
				        sh 'echo $USER'
			            }
		          }
        
    
         stage('Building image') {
                steps{
                script {
                    dockerImage = docker.build registry + ":$BUILD_NUMBER"
                    }
                }
            }
           }
         }  
