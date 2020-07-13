node{
  stage('Git-Checkout'){
    git 'https://github.com/ramyashanmukha/Jenkins'
  }
  stage('Compile-Package'){
    def mvnHome = tool name: 'Maven', type: 'maven'
    sh '$(mvnHome)/bin/mvn package'
  }
}
