pipeline {
    agent any

    stages{
        stage('git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Le-Moktar/s2-w13-awscicd.git'
            }
        }
        stage('test '){
            steps{
               sh "echo test" 
            }
        }
    }
}