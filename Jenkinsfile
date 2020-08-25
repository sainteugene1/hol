pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sleep 1
            }
        }
    }stage('build') {
            steps {
                echo 'Hello build'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                
                 sleep 1 
            }
            }
        }stage('deploy') {
            steps {
                echo 'Hello deploy'
                sleep 1
            }
        }
}stage('test') {
            steps {
                echo 'Hello test'
                sleep 1
            }
        }
