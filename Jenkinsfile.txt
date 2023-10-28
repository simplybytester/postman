pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                sh 'echo "hello"'
            }
        }
        stage('Add repository') {
            steps {
                git branch: 'main', url: 'https://github.com/simplybytester/postman.git'

            }
        }
         
    }
}
