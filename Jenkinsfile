def dockerImage
pipeline {
  agent any
    stages {
      stage('teststage') {
        steps {
           echo "multi stage pipeline test"
           script {
               dockerImage = docker.build("8cd5b94f1c1ca7bd0a2d1065feb708e5.loophole.site/buildimg:v1")
           }
        }
      } 
      
      stage('push image') {
        steps {
           echo "multi stage pipeline test"
           script {
               dockerImage.push("custompushtag")
           }
        }
      } 
    }
}
