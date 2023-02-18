pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -c working.cpp'
                sh 'g++ -o working working.cpp'
                eco 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh './working'
                echo 'Test was successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy steps successful'
            }
        }
        
    }
    post{
       failure{
      echo 'Pipelined failed'
       }
    }
}
