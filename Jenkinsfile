@Library("shared-lib") _ 
pipeline {
    agent { label 'docker' }
    options { timestamps() }
    environment {
        GIT_CRED        = credentials('Github-Read')
        PYPI            = credentials('pypi-admin-creds')
        SECRET_FILE     = credentials('version-file')
    }
    stages {
        stage('Build an Updated Tag') {
            steps {
                script {
                    semanticVersionAi{
                        GIT_CRED_PSW = GIT_CRED_PSW
                        PYPI_USR     = PYPI_USR
                        PYPI_PSW     = PYPI_PSW
                    }
                }
            }
        }
    }
}
