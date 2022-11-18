pipeline {
    agent any
    stages {
        stage('Do everything in parallel') {
            parallel {
            stage('Build') {
                agent {
                    label "default"
                }
                    echo 'Building..'
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
                    label "default"
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
