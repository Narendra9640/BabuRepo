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
               
                    goals: 'clean install',
                    deployerId: "MAVEN_DEPLOYER",
                    resolverId: "MAVEN_RESOLVER"
            }
        }

       
    }
}
