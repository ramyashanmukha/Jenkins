pipeline {
    agent any

    environment{
      PATH = "/opt/maven/bin:$PATH"
    }
  
    stages {
        stage('Git') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ramyashanmukha/Jenkinshttps://github.com/cameronmcnz/rock-paper-scissors'
            }
        }
      stage('Build'){
        steps{
          sh "mvn clean package"
        }
      }
        stage('Deployment'){
            steps{
                deploy adapters: [tomcat9(credentialsId: '9b33adf8-11e5-4e09-91d1-08a0d22f961d', path: '', url: 'http://ec2-3-85-141-136.compute-1.amazonaws.com:8008/')], contextPath: '/Pipeline', war: '**/*.war'
            }
        }  
    }
}
