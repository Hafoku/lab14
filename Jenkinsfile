pipeline {
    agent any

    stages {
        stage('Checkout') {
            git 'https://github.com/<organization>/<project>.git'
        }
        stage('Build') {
            steps {
                sh 'python setup.py install'
            }
        }
        stage('Test') {
            steps {
                sh 'python -m unittest tests'
            }
        }
    }
}
