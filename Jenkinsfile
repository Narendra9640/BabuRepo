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
        
          stage('package') {
            steps {
                sh 'mvn package'
            }
        }
        
        
          stage('DOCKER_IMAGE') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com','dockerhub'){
                        
                        myimage=    docker.build("narendra96/pipelinedemo")
                        
                        myimage.push()
                    }
                }
            }
          }
        
        
       
    }
}
