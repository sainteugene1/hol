pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }
    triggers {
  pollSCM '* * * * *'
}

    stages {
        
       stage('build') {
            steps {
                echo 'Hello build'
                sh 'mvn clean'
                sh  'mvn install'
                sh 'mvn package'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
                
            }
        }
        stage ('build and publish image') {
      steps {
        script {
          checkout scm
          docker.withRegistry('', 'DockerUserID') {
          def customImage = docker.build("sainteugene1/devops-pipeline:${env.BUILD_ID}")
          def customImage = docker.build("sainteugene1/devops-pipeline")
          customImage.push()
          customImage.push()
    }
        
    }
}
    }

