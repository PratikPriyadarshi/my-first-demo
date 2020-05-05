node{
  stage('SCM Checkout'){
    git 'https://github.com/PratikPriyadarshi/my-first-demo'
  }
  stage('Compile-Package'){
    sh 'mvn package'
  }
}
