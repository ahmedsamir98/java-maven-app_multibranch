pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                script {
                    echo "########## testing the application ########"
                    echo "#####===== this is branch $BRANCH_NAME ====####"
                }
            }
        }
        stage('build') {
            when{
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "########## building the application ########"
                }
            }
        }
        stage('deploy') {
            when{
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "########## seploying the application ########"
                }
            }
        }
    }
}
