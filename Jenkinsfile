pipeline {
    agent any 

       tools {
        maven 'maven'    }
    stages {

         stage('variables') {
            steps {
               script {
                   echo $env.BRANCH_NAME
                 }
            }
        }

         stage('diff') {
            steps {
               script {
                  sh ' git diff origin/branch2'
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
