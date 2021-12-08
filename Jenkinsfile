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
                ls -lrt 
                docker cp "/root/workspace/ne_JM_Multibranch_BranchItaliano/target/sparkjava-hello-world-1.0.war" tomcat_ita:"/usr/local/tomcat/webapps"
                '''
                  }
        
        }
    }
}
