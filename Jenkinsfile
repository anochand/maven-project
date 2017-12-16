pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh '/home/anoop/Documents/apache-maven-3.5.2/bin/mvn clean package'
           }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                 }
           }
         }
    }
}
