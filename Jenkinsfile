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
        disableConcurrentBuilds()
        }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                echo  "this is shell script.."
                echo "$GREETING"
                #sleep 10
               """
            }
        }
        stage('check params') {
            steps {
                sh """
                  echo "Hello ${params.PERSON}"

                  echo "Biography: ${params.BIOGRAPHY}"

                  echo "Toggle: ${params.TOGGLE}"

                  echo "Choice: ${params.CHOICE}"

                  echo "Password: ${params.PASSWORD}"
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
            echo 'this runs when it is successss'
        }
    }
}