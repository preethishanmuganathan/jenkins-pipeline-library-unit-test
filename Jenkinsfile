node {
    
    stages {
        stage('checkout') {
            checkout scm
        }
        stage('Build') {
            steps {
                mvn(goals: 'clean compile')
            }
        }
        stage('Test'){
            steps {
                mvn(goals: 'test')
            }
        }
        stage('Publish') {
            steps {
                junit 'target/surefire-reports/TEST*.xml'
            }
        }
    }
}
