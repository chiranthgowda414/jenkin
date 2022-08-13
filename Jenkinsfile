pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                git branch: 'main', url: 'https://github.com/chiranthgowda414/cproject.git'
                sh '''
                    #!/bin/bash
                    pwd
                    ls
                    echo "This is a BUILD stage"
                '''
            }
        }

        stage('DEPLOY') {
            agent { label 'label' }
            steps {
                echo "This is a DEPLOY stage"

            }
        }

        stage('TESTING1') {
            agent { label 'label' }
            steps {
                sh 'echo "This is a TESTING1 stage"'

            }
        }

        stage('TESTING2') {
            agent { label 'master' }
            steps {
                sh '''
                    echo "This is a TESTING2 stage"

                '''
            }
        }
    }
}
