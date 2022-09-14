pipeline {
    agent any
    //environment {
    //    SECRET_FILE_ID = credentials('gehc-creds')
    //}
    stages {
        stage('Hello') {
            steps {
                echo 'Starting......'
                script {
                    load "jenkins.env"
                    echo "from grovvy : ${env.DEPLOY_BASE_URL}"
                    sh """
                        #!/usr/bin/env bash
                        echo "from Shell : ${DEPLOY_BASE_URL}"
                    """
                }
            }
        }
    }
}
