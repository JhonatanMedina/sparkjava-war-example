pipeline {
    agent { node { label "Jhonatan" } }
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                '''
            }
         stage('build') {
            steps {
                sh '''
                echo "hola Mundo"
                '''
            }
        stage('Deployar') {
            steps {
                sh '''
                echo "hola Mundo deployado"
                '''
            }
        }
    }
}
