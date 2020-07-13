pipeline {
    agent any

    environment{
      PATH = "/opt/maven/bin:$PATH"
    }
  
    stages {
        stage('Git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ramyashanmukha/Jenkins'
            }
        }
      stage('Build'){
        steps{
          sh "mvn clean package"
        }
      }      
    }
}
