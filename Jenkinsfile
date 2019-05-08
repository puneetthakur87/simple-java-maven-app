pipeline {
    agent any
     parameters{
          choice(name: 'Select the RUN type for the Job', choices: '—dry-run\n\n—hot-run', description: 'Trying Parameterized Job')
              }           

stages {

        stage('Build') {

            steps {

                echo 'Building the Job...'

            }

        }

        stage('Test') {

            steps {

                parallel (

          Phase1: {

            echo "Phase 1 Testing"

          },

          Phase2: {

            echo "Phase 2 Testing"

          },

          Phase3: {

            echo "Phase 3 Testing"

          }

        )

            }

        }

        stage('Deploy') {

            steps {

                echo 'Deploying the Job....'

            }

        }

    }

}
