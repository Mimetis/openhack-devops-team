pipeline {
    agent any

    stages {
        stage('poi') {
            steps {
                echo 'poi'
            }
        }
        stage('trips') {
            agent {
                docker { image 'golang:1.8' }
            }
            steps {
                sh 'cd apis/trips; go test ./test'
            }
        }
        stage('user-java') {
            steps {
                echo 'user-java'
            }
        }
        stage('userprofile') {
             steps {
                 echo 'userprofile'
             }
         }
    }
}
