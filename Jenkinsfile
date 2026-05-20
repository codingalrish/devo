pipeline {
   agent any

   stages {

       stage('Build with Maven') {
           steps {
               echo 'Building Project...'
               sh 'mvn package'
           }
       }

       stage('Show Artifact') {
           steps {
               sh 'ls target'
           }
       }
   }

   post {

       success {
           echo 'Build Successful - Sending Email'
       }

       failure {
           echo 'Build Failed - Sending Email'
       }
   }
}
