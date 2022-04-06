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
                sh "sudo rm -rf /var/www/html/jenkins_st"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/html/jenkins_st/"
            }
        }
    }
}
