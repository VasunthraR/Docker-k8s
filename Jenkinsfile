node{
  
  stage('code build'){
    git 'https://github.com/VasunthraR/simpleapp'
  }
  stage('build') {
    def mvnHome = tool name: 'maven3', type: 'maven'
    sh "${mvnHome}/mvn clean install"
  }
  stage('Build Docker Image'){
     sh 'docker build -t my-app .'
   }
 
}  
