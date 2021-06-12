node {

stage('SCM Checkout'){
git 'https://github.com/Narendra9640/BabuRepo.git'
}
stage('Complie-package'){
  def mvnHome = tool name: 'Maven1', type: 'maven'
  sh "${mvnHome}/bin/mvn package"
}
}
