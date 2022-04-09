pipeline {
    agent any
    stages {
        stage('Stage') {
            steps {
                echo 'Deploying in staging environment'
                git  'https://github.com/princesarvaiya/docker.git'
            }
        }
        stage('Testing') {
            steps {
                echo "Perform UNIT testing"
            }
        }
        
         stage('Building') {
            steps {
                echo "Build a docker image using the Dockerfile and name it webapp-color"
				script{
                    image = docker.build("princesarvaiya/webapp-color")
                }
            }
        }
        stage('Running container'){
            steps {
                script{
                      sh "docker run -itd -e APP_COLOR=green -p 8282:8080 princesarvaiya/webapp-color"
                }
              
            }
            
        }

	}
}
