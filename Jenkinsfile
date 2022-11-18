pipeline {
    agent any
    stages {
        stage('Do everything in parallel') {
            parallel {
            stage('Build') {
                steps {
                    echo 'Building..'
                }
            }
            stage('Test') {
                agent {
                    lable "linux"
                }
                steps {
                    echo 'Testing..'
                }
            }
            stage('Deploy') {
                steps {
                    sh "cat hello.txt"
                    echo 'Deploying....'
                }
            }
        }
            }
        }
}