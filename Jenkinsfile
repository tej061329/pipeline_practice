pipeline {
    agent any 
    stages{
        stage('build') {
            steps{
                 sh '''
                    sleep 5
                    echo "This is a build stage"
                    echo "welcome"
                '''
            }
        }

        stage('test') {
            
            parallel {

                stage('TEST ON LINUX MACHINE') {
                    steps {
                        sh '''
                            sleep 6
                            echo "This is a TEST on LINUX"
                            exit 0
                        '''
                    }
                }
            stage('TEST ON WINDOWS MACHINE') {
            steps{
                sh '''
                    sleep 6
                    echo "This is a test stage"
                    echo "continue"
                    '''
            }
        }
            }
        }
        stage('DEPLOY') {
            steps{
                sh '''
              echo "this is the last and deploy stage"
              echo "END"
              '''
            }
        }
    }
}
