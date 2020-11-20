pipeline {
    agent any
    
    stages{
       stage('Build'){
           steps{
               echo 'hello world'
               build {
                job:'pipeline-hello-world',
                parameters: [
                  string(name:'CHOICE',value:'dev')
                ]
              }
           }
       } 
    }
    parameters {
        choice(name: 'CHOICE', choices: ['dev', 'prod'], description: '构建的环境，默认为dev')
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