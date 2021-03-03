pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      //maven "mvn 3.3.9"
      def mvn_version = 'M3'
      withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
        //sh "mvn clean package"
      }
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