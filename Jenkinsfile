pipeline {
    agent any

    parameters {
        string (name: 'APP_NAME', defaultValue: 'my_app', description: 'application name')
        choice (name: 'ENVIRONMENT', choices: ['dev','uat','prod'], description: 'environment')
        booleanParam (name: 'RUN_TEST', defaultValue: true, description: 'run test cases')
    }

    stages {

        stage("build") {
            steps {
                echo "[=== BUILD STEPS ===]"
            }
        }

        stage("test") {
            when {
                expression {
                    params.RUN_TEST == true
                }
            }
            steps {
                echo "[=== TEST STEPS ===]"
            }
        }

        stage("deploy") {
            steps {
                echo "[=== DEPLOY STEPS ===]"
                echo "Deploying applicaiton ${params.APP_NAME} in Environment: ${params.ENVIRONMENT}"
            }
        }

    }
}
