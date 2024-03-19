pipeline{
    agent {
      node {
         label 'AGENT-1'
       }
    }


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
}