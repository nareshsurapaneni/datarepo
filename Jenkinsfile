pipeline {
    agent any 

       tools {
        maven 'maven'    }
    stages {

        stage('Checkout') {
            steps {
                script {
                    // Checkout the current branch
                    checkout scm
                }
            }
        }

         stage('variables') {
            steps {
               script {
                   sh 'echo "Hello world" > a.txt'
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
