pipeline {
    agent any
    
    stages{
      stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
       stage('Build'){
         input {
              message "Should we continue?"
              ok "Yes, we should."
              submitter "alice,bob"
              parameters {
                  string(name: 'PERSON', defaultValue: 'TEST', description: 'Who should I say hello to?')
              }
          }
           steps{
               echo "Hello ${params.BUILD_ENV}-${PERSON}"
           }
       } 
    }

    options { buildDiscarder(logRotator(numToKeepStr: '3')) }

    parameters {
        choice(name: 'BUILD_ENV', choices: ['dev', 'prod'], description: '构建的环境，默认为dev')
    }
    
    post {

      always{
        echo 'always'
      }
      changed{
        echo 'status changed'
      }
      success {
        echo 'success'
      }
      failure {
        echo 'failure'
      }
      cleanup{
        echo 'cleanup'
      }
    }
}