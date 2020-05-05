node{
  stage('SCM Checkout'){
    git 'https://github.com/PratikPriyadarshi/my-first-demo'
  }
  //stage('Compile-Package'){
    //Get maven home path
    //def mvnHome = tool name: 'maven-3', type: 'maven'
    //sh "${mvnHome}/bin/mvn package"
  //}
  stage('Build') {
        def mvn_version = 'M3'
        withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
        sh '''for f in i7j-*; do
                (cd $f && mvn clean package -Dmaven.test.skip=true -Dadditionalparam=-Xdoclint:none  | tee ../jel-mvn-$f.log) &
              done
              wait'''
        }
   }
}
