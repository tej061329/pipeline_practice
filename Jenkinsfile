pipeline {
    agent any 
    stages{
        stage('build') {
            steps{
                 catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                 sh '''
                    sleep 5
                    echo "This is a build stage"
                    echo "welcome"
                    exit 1
                '''
            }
        }
        }
        stage('test') {
            
            parallel {

                stage('TEST ON LINUX MACHINE') {
                    steps {
                        sh '''
                            sleep 6
                            echo "This is a TEST on LINUX"
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
             stage('TEST ON MAC MACHINE') {
            steps{
                sh '''
                    sleep 6
                    echo "This is a test stage"
                    echo "continue"
                    '''
            }
        }   
               stage('TEST ON CHROME MACHINE') {
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
