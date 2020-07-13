node{
  stage('Git-Checkout'){
    git 'https://github.com/ramyashanmukha/Jenkins'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
}
