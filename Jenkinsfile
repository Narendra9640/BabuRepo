pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps {
                git branch: 'main', url: "https://github.com/Narendra9640/BabuRepo.git"
            }
        }

        
        
        
     stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
       
    }
}
