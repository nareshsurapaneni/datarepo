pipeline {
    agent any 

       tools {
        maven 'maven'    }
    stages {
        stage('Build') {
            steps {
               script {
                  sh 'mvn clean install'
               }
            }
        }
    }
}