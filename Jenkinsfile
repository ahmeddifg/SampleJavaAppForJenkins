pipeline {

    agent any

    stages {
        stage('Build') {
            steps {
                 echo 'Build'
                 sh '/var/jenkins_home/jenkins-pipline1.mvn.sh  mvn -B -DskipTests clean package'
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
