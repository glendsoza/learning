pipeline {
    agent any
    stages {
        stage('Do everything in parallel') {
            parallel {
            stage('Build') {
                agent {
                    label "Built-In Node"
                }
                steps {
                    echo 'Building..'
                }
            }
            stage('Test') {
                agent {
                    label "linux"
                }
                steps {
                    sh "cat hello.txt"
                    echo 'Testing..'
                }
            }
            stage('Deploy') {
                agent {
                    label "Built-In Node"
                }
                steps {
                    sh "cat hello.txt"
                    echo 'Deploying....'
                }
            }
        }
            }
        }
}