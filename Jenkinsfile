pipeline{
    agent {
      node {
         label 'AGENT-1'
       }
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
                echo 'Deploy...'
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
            echo 'success'
        }
    }
}