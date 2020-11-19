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
        success {
          script {
            mail to: 'yinglichen@xiaoman.cn', 
            subject:'The Pipeline success mail test',
            body:'The Pipeline success mail test'
          }
        }
        failure {
          script {
            mail to: 'yinglichen@xiaoman.cn', 
            subject:'The Pipeline faild mail test',
            body:'The Pipeline faild mail test'
          }
        }
    }
}