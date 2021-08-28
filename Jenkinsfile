pipeline {
   agent any
   stages {
      stage('Checkout') {
         steps {
            checkout scmm
            def customImage = docker.build("my-image:${env.BUILD_ID}")
            customImage.inside {
            sh 'make test'
           
         }
      }
   
    stage('Build') {
         steps {
            customImage.push('latest')
           
         }
      }  
    stage('Deploy') {
         steps {
            echo 'Deploy'
         }
      }
    stage('Test') {
         steps {
            echo 'Test'
         }
      }    
   }
}
