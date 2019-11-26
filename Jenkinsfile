pipeline {

    agent any

    stages {
        stage('Build') {
            steps {
                 echo 'Build'
                 sh '/var/jenkins_home/jenkins-pipline1/mvn.sh'
                 sh '/var/jenkins_home/jenkins-pipline1/build.sh'
            }

            post {
                success {
                  echo 'Build success'
                }
            }
        }

        stage('Test') {
            steps {
             echo 'Test'
             sh '/var/jenkins_home/jenkins-pipline1/mvntest.sh'
            }

            post {
                always {
                   echo 'Test success'
                }
            }
        }

        stage('Push') {
            steps {
            echo 'Push'
            }
        }

        stage('Deploy') {
            steps {
              echo 'Deploy'
            }
        }
    }
}
