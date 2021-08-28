pipeline {
   agent any
   stages {
      stage('Checkout') {
         steps {
            echo 'Code Checkout'
         }
      }
    stage('Compile') {
         steps {
            echo 'Compile'
         }
      }  
    stage('Build') {
         steps {
            echo 'Build'
            FROM nginx:latest
            COPY . /usr/share/nginx/html
            EXPOSE 80
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
