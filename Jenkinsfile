pipeline{
    agent any

    stages{
        stage("Sonar Quality check"){
            agent {
                docker {
                    image 'openjdk:11'
                }
                        
                  }
            steps{
                script{
                     withSonarQubeEnv('sonarserver') {
                      sh 'chmod +x gradlew'
                      sh './gradlew sonarqube'
                     }
                    }
                }
            }
        }
    }