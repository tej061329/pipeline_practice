pipeline {
    agent any 
    stages{
        stage('FIRST') {
            steps{
                 sh '''
                    sleep 5
                    echo "This is a FIRST stage"
                    echo "welcome"
                '''
            }
        }

        stage('SECOND') {
            steps{
                sh '''
                    sleep 6
                    echo "This is a second stage"
                    echo "continue"
                    '''
            }
        }

        stage('DEPLOY') {
            steps{
                sh '
              echo "this is the last and deploy stage"
              '
            }
        }
    }
}
