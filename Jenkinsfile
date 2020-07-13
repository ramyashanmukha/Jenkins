pipeline {
    agent any

   /* tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }*/

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
