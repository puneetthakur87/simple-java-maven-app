pipeline {
    agent any
    parameters{
          choice(name: 'Select the RUN type for the Job', choices: '—dry-run \n —hot-run', description: 'Trying Parameterized Job')
              }           

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
