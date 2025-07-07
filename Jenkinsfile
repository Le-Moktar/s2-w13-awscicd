pipeline {
    agent any

environment {
    BRANCHE_NAME = 'main'
    GIT_URL = 'https://github.com/Le-Moktar/s2-w13-awscicd.git'
    IMAGE_TAG = 'moktar/awscicd'
    IMAGE_VERSION = '${BUILD_NUMBER}'
}
    stages{
        stage('git checkout'){
            steps{
                git branch: "${BRANCHE_NAME}", url: "${GIT_URL}"
            }
        }
        stage('Docker build'){
            steps{
               sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .' 
               sh 'docker images'
            }
        }
    }
}