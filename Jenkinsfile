node{
  stage('SCM Checkout'){
    git 'https://github.com/PratikPriyadarshi/my-first-demo'
  }
  stage('Compile-Package'){
    
   //Get maven home path
    def mvnHome = tool name: 'maven', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
   
}
