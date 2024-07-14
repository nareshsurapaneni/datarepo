pipeline {
    agent any 

       tools {
        maven 'maven'    }
    stages {

         stage('diff') {
            steps {
               script {
                  sh ' git diff branch2'
               }
            }
        }

        stage('Build') {
            steps {
               script {
                  sh 'mvn clean install'
               }
            }
        }
    }
}