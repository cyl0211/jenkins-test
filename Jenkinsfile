pipeline {
    agent any

    environment { 
        CC = 'chen'
        // AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
        // AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
    }
    
    stages{
      stage('Example') {
        environment { 
                DEBUG_FLAGS = '-g'
            }
            steps {
                echo "${CC}"
            }
        }
       stage('Build'){
        //  input { 
        //       message "Should we continue?"
        //       ok "Yes, we should."
        //       submitter "alice,bob"
        //       parameters {
        //           string(name: 'PERSON', defaultValue: 'TEST', description: 'Who should I say hello to?')
        //       }
        //   }
           steps{
               echo "Hello ${params.BUILD_ENV}-${PERSON}"
           }
       } 
    }

    options { buildDiscarder(logRotator(numToKeepStr: '3')) }

    // parameters {
    //     choice(name: 'BUILD_ENV', choices: ['dev', 'prod'], description: '构建的环境，默认为dev')
    // }
    
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