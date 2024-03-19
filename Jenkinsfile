pipeline{
    agent {
      node {
         label 'AGENT-1'
       }
    }
    environment{
        GREETING = 'Jenkins...'
    }
    options{
        timeout(time: 1,unit: 'HOURS')
        disableConcurentBuilds()
        }
    

   //build
    stages{
        stage('Build'){
            steps{
                echo 'Bulding...'
            }
        }
        stage('Test'){
            steps{
                echo 'Testig...'
            }
        }
        stage('Deploy'){
            steps{
               sh """
                echo  "this is shell script"
                echo "$GREETING"
                sleep 10
               """
            }
        }
    }
    //post build
    post{
        always{
            echo 'always ...'
        }
        failure{
            echo 'this runs when it is failure,user added send some alerts'
        }
        success{
            echo 'this runs when it is success'
        }
    }
}