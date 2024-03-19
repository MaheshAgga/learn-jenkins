pipeline{
    agent {
      node {
         label 'AGET-1'
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