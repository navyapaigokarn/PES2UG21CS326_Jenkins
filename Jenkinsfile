pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh "g++ -o output PES2UG21CS326-1.cpp"
            }
        }
        stage('Test') {
            steps {
                sh "./output"
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post { 
        failure { 
            error "Pipeline failed"
        } 
    } 
}
