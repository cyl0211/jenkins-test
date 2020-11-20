pipeline {
    agent any
    
    stages{
       stage('Build'){
           steps{
               echo "Hello ${params.BUILD_ENV}"
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