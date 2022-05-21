pipeline {
    agent any
    tools {
  maven 'M2_HOME'
}
    triggers {
  pollSCM('* * * * *')
    }
    stages {
        stage('maven packakge') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
          stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
          stage('Deploy') {
            steps {
                echo 'Deploy step'
                sleep 5
            }
        }
          stage('Docker') {
            steps {
                echo 'Image stape'
            }
        }
    }
}
