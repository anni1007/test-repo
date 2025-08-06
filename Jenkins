pipeline {
    agent any
    
    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['dev', 'qa', 'prod'],
            description: 'Select the environment'
        )
    }
    stages {
        stage('Checkout') {
            steps {
               git url: 'https://github.com/anni1007/test-repo.git', branch: 'main'
            }
        }

    stage('Deploy') {
            steps {
                script {
                    echo "Selected environment: ${params.ENVIRONMENT}"

                    if (params.ENVIRONMENT == 'dev') {
                        echo 'Executing DEV deployment...'
                        // sh './deploy_dev.sh'
                    } else if (params.ENVIRONMENT == 'qa') {
                        echo 'Executing QA deployment...'
                        // sh './deploy_qa.sh'
                    }
                    else if (params.ENVIRONMENT == 'prod') {
                        echo 'Executing PROD deployment...'
                        // sh './deploy_prod.sh'
                    }
                }
            }
        }
    }
}
