pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "Mvn 3.3.9"
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