pipeline {
    agent any

    environment {
        MY_VARIABLE = 'value'
        MY_CREDENTIAL = credentials('credential_id')
    }

    stages {

        stage("build") {
            steps {
                echo "[=== BUILD STEPS ===]"
            }
        }

        stage("test") {
            steps {
                echo "[=== TEST STEPS ===]"
                echo "My variable value: ${MY_VARIABLE}"
            }
        }

        stage("deploy") {
            steps {
                echo "[=== DEPLOY STEPS ===]"
                echo "Credential to remote login: ${MY_CREDENTIAL}"   // Note: Don't print it in actual pipeline.
            }
        }

    }
}
