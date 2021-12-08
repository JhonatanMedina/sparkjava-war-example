pipeline {
    agent { node { label "Jhonatan" } }
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                echo $JM_parametro
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
                docker cp "/root/workspace/FolderJM/Pipeline_JM/target/sparkjava-hello-world-1.0.war" condescending_borg:"/usr/local/tomcat/webapps"
                '''
                  }
        
        }
    }
}
