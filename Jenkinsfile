pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES2UG20CS160-1', wait: false
                 echo 'Build by CS160 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by CS160 successful'
            }
        }

        stage('Deploy') {
            steps {
              
                echo 'Deploy by CS160 successful'
            }
        }
    }

    post {
        failure {
           
                echo 'Pipeline Failed'
         
        }
    }
}
