pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the code from your GitHub repository
                checkout([$class: 'GitSCM', 
                    branches: [[name: 'main']], 
                    doGenerateSubmoduleConfigurations: false, 
                    extensions: [], 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[url: 'https://github.com/MohitThakur051998/jenkins_test.git']]
                ])
            }
        }

        stage('Deploy to Apache') {
            steps {
                // Copy the code to the Apache document root directory
                bat script: '''
                    xcopy /s /e /y "C:\\Users\\mohit\\OneDrive\\Desktop\\New folder (2)" "C:\\Apache24\\htdocs"
                '''
            }
        }
    }
}
