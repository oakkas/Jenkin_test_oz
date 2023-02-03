pipeline{
    agent any
    environment{
        GITHUB_CREDS = credentials("github_creds")
    }
    parameters{
        string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod')
        choice(name: 'VERSION_CHOICE', choices: ['1.1.0', '1.2.0', '1.3.0'], description: ''])
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages{
        stage("build"){
            steps{
                echo "Building the app at ${BRANCH_NAME}"
                echo "EXECUTOR_NUMBER: ${EXECUTOR_NUMBER}"
                echo "NODE_NAME: ${NODE_NAME}"
                echo "WORKSPACE: ${WORKSPACE}"
                echo "WORKSPACE_TMP: ${WORKSPACE_TMP}"
                echo "GITHUB CREDS: ${GITHUB_CREDS}"
            }
        }
        stage("test"){
            when{
                expression{
                    params.executeTests
                }
            }
            steps{
                echo "Testing the app at ${BRANCH_NAME}"
                echo "Execute test ${params.executeTests}"
            }
        }
        stage("deploy"){
            steps{
                echo "Deploying the app at ${BRANCH_NAME}"
                echo "Deploying VERSION: ${params.VERSION_CHOICE}"
            }
        }
    }
}