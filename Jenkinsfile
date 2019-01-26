pipeline {
    agent any
     tools {
        maven 'localMaven'
    }
    stages{
        stage('Build'){
            steps {
                batch 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
