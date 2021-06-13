node {
  stage ('Build') {
    git url: 'https://github.com/Narendra9640/BabuRepo.git'
    withMaven {
      sh "mvn clean verify"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}
