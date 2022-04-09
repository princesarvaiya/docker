pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        sh '''echo "Build Docker image"
image = docker.build("princesarvaiya/webapp-color")
echo "=============================================="
echo "Running container"
sh "docker run -itd -e APP_COLOR=green -p 8282:8080 princesarvaiya/webapp-color"'''
      }
    }

  }
}