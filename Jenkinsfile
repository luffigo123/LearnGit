pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }

        stage('environment to test When') {
            when {
                allOf {
                    //branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
