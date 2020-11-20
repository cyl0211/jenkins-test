pipeline {
    agent any
    
    stages{
       stage('Build'){
           steps{
               echo 'hello world'
           }
       } 
    }
    parameters {
        choice(name: '构建环境', choices: ['dev', 'prod'], description: '构建的环境，默认为dev')
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