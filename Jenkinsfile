pipeline {
    agent { node { label "Jhonatan" } }
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                '''
            }
        }
         stage('build') {
            steps {
                sh '''
                mvn clean install
                '''
            }
         }
        stage('Deployar') {
            steps {
                sh '''
                docker cp "/root/workspace/Pipeline_JM/target/sparkjava-hello-world-1.0.war" hungry_meninsky:"/usr/local/tomcat/webapps"
                '''
                  }
        
        }
    }
}
