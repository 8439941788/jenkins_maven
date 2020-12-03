pipeline{
    agent any
    stages{
        stage('cloning repository and cleaning maven'){
          steps{
                sh "mvn clean"
                
            }
        }
        stage('testing'){
            steps{
                sh "mvn test"
                
            }
        }
        stage('packaging'){
            steps{
                sh "mvn package"
                
            }
        }
        stage('archiving'){
            steps{
                archiveArtifact '**/target/*.jar'
                
            }
        }
    }
}
