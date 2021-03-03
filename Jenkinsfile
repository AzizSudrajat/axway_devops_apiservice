pipeline {
   agent any

   tools {
      maven 'M3'
   }

   stages {
      stage('Build') {
         steps {
            // Get the repository from GitHub
            git 'https://github.com/AzizSudrajat/axway_devops_apiservice.git'

            // Run Maven 
            sh "mvn clean exec:java"
         }
      }
   }
}