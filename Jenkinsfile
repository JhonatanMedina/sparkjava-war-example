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
                docker cp "/root/workspace/ine_JM_Multibranch_BranchEspa_ol/target/sparkjava-hello-world-1.0.war" tomcat_esp:"/usr/local/tomcat/webapps"
                '''
                  }
        
        }
    }
}
