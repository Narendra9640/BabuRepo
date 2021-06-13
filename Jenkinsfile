pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps {
                git branch: 'main', url: "https://github.com/Narendra9640/BabuRepo.git"
            }
        }

    

        stage ('Exec Maven') {
            steps {
                rtMavenRun (
                    tool: MAVEN_TOOL, // Tool name from Jenkins configuration
                    pom: 'maven-example/pom.xml',
                    goals: 'clean install',
                    deployerId: "MAVEN_DEPLOYER",
                    resolverId: "MAVEN_RESOLVER"
                )
            }
        }

       
    }
}
