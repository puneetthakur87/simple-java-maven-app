pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                parallel (
          firefox: {
            echo "Firefox Testing"
          },
          Chrome: {
            echo "Chrome Testing"
          },
          IE: {
            echo "IE Testing"
          },
          Mobile: {
            echo "Mobile Testing"
          }
        )
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
