pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'jdk8'
    }
    parameters {
        booleanParam(name: "Perform release ?", description: '', defaultValue: false)
    }
    stages {
        stage('Initialize') {
            steps {
                sh '''
                    echo "Initialisation du build"
                '''
            }
        }
        stage('Build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
