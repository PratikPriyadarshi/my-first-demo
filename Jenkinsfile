node{
  stage('SCM Checkout'){
    git 'https://github.com/PratikPriyadarshi/my-first-demo'
  }
  stage('Compile-Package'){
    
   //Get maven home path
    def mvnHome = tool name: 'Maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
   
}
