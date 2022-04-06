pipeline {
    agent any
   
    stages {
        stage('Test') {
            steps {
                sh 'yarn'
                sh 'yarn test'
            }
        }
        stage('Build') {
            steps {
                sh 'yarn'
                sh 'yarn build'
            }
        }
        stage('Deploy') {
            steps {
                sh "rm -rf /var/www/jenkins_st"
                sh "cp -r ${WORKSPACE}/build/ /var/www/jenkins_st/"
            }
        }
    }
}
