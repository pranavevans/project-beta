pipeline {
    agent any
    stages {
        stage('Okayyy') {
            steps {
                echo "Ok"
            }
        }
    }
    
    
    post {
        success {
            emailext (
                to: sripurampranav@gmail.com,
                subject: "SUCCESS",
                body: "SUCCESS!  '${env.JOB_NAME} [${env.BUILD_NUMBER}]'"
            )
        }
        failure {
			emailext (
                to: sripurampranav@gmail.com,
                subject: "FAILURE",
                body: "FAILURE!  '${env.JOB_NAME} [${env.BUILD_NUMBER}]'"
            )
        }
    }
}
