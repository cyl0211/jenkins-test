pipeline {
    agent any
    
    stages{
       stage('Build'){
           steps{
               echo 'hello world'
           }
       } 
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