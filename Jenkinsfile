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
            mail to: '2424084898@qq.com', 
            subject:'The Pipeline success mail test',
            body:'The Pipeline success mail test'
          }
        }
        failure {
          script {
            mail to: '2424084898@qq.com', 
            subject:'The Pipeline faild mail test',
            body:'The Pipeline faild mail test'
          }
        }
    }
}